$$ PPL(X) = e^{CE(X)}$$

$$ = e^{-\frac{1}{t}\sum_{i=0}^t \log p(x_i| x_{<i})} $$

```python
loss = model(input_ids=inputs["input_ids"],
			 labels=inputs["input_ids"]).loss
ppl = torch.exp(loss)

print(f"Perplexity: {ppl.item():.2f}")
>>> Perplexity: 4.26
```
