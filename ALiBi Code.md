-
[ALiBi GitHub](https://github.com/ofirpress/attention_with_linear_biases#readme)

> The implementation is very simple.
> \ - @ofirpress

`transformer.py:693`
```python
self.embed_positions = (
	PositionalEmbedding(
		self.max_target_positions,
		embed_dim,
		self.padding_idx,
		learned=args.decoder_learned_pos,
	)
	if not args.no_token_positional_embeddings
	else None
)
```

`transformer.py:920`
```python
# embed positions
positions = None
# if self.embed_positions is not None:
#    positions = self.embed_positions(
#        prev_output_tokens, incremental_state=incremental_state
#    )
```

- Remove the position embeddings from the model
`transformer.py:941`
```python
# if positions is not None:
#    x += positions
```

- Set up the relative bias matrix, here
`transformer.py:742`
```python
def get_slopes(n):
	def get_slopes_power_of_2(n):
		start = (2**(-2**-(math.log2(n)-3)))
		ratio = start
		return [start*ratio**i for i in range(n)]

	if math.log2(n).is_integer():
		return get_slopes_power_of_2(n)                   #In the paper, we only train models that have 2^a heads for some a. This function has
	else:                                                 #some good properties that only occur when the input is a power of 2. To maintain that even
		closest_power_of_2 = 2**math.floor(math.log2(n))  #when the number of heads is not a power of 2, we use this workaround. 
		return get_slopes_power_of_2(closest_power_of_2) + get_slopes(2*closest_power_of_2)[0::2][:n-closest_power_of_2]
```

- Add the bias matrix to the mask, which is then added in each attention score computation
`transformer.py:1011`
```python
def buffered_future_mask(self, tensor):
	dim = tensor.size(1)
	# self._future_mask.device != tensor.device is not working in TorchScript. This is a workaround.
	if (
		self._future_mask.size(0) == 0
		or (not self._future_mask.device == tensor.device)
		or self._future_mask.size(1) < self.args.tokens_per_sample
	):
		self._future_mask = torch.triu(
			utils.fill_with_neg_inf(torch.zeros([self.args.tokens_per_sample, self.args.tokens_per_sample])), 1
		)
		self._future_mask = self._future_mask.unsqueeze(0) + self.alibi
	self._future_mask = self._future_mask.to(tensor)
	return self._future_mask[:tensor.shape[0]*self.args.decoder_attention_heads, :dim, :dim]
```

- Move the mask computation to before the layer loop, to make the transformer a tiny bit faster  (This might not be necessary in other frameworks.) 
`transformer.py:949`
```python
#We move the mask construction here because its slightly more efficient.
if incremental_state is None and not full_context_alignment:
	 self_attn_mask = self.buffered_future_mask(x)
else:
	 self_attn_mask = None
# B x T x C -> T x B x C
x = x.transpose(0, 1)
```