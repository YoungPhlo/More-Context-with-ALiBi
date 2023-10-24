[Source: Ofir Press](https://ofir.io/The-Use-Case-for-Relative-Position-Embeddings/)

![](relative-its-cleaner.jpg)

> We’re in 2022 but many of our most popular causal language models (LMs), including GPT-3, still use absolute positional embeddings. I believe we should stop using those and move to relative positional embeddings such as ALiBi.

> Imagine you’re building the next version of a causal code prediction model like Codex. When we train an LM like this, due to GPU memory limitations, we must pick a finite sequence length, say 4,000 tokens, to train the model on. If at inference time, users only want to make predictions in code files shorter than 4,000 tokens, we’re good. But if a user wants to make a prediction for token 4,001, it would be impossible with absolute position embeddings. If you use learned position embeddings, feeding 4,001 tokens to your LM will simply throw a runtime exception (there is no 4,001 position representation). If you use [[Why sinusoidal doesn't extrapolate|sinusoidal position embeddings]], the model will run given 4,001 inputs, but as we show in the [[PDF Train Short, Test Long - ALiBi|ALiBi paper]], it will produce really bad predictions (for any token beyond the first 4,000).

> The rotary ([[ALiBi vs RoPE|RoPE]]) method has shown some strong results when evaluating sequences that are shorter than or equal to train length, but in our paper we show that it is not able to extrapolate to longer sequences.

> *Can’t I just use an absolute position method and a sliding window to extrapolate?*
> Short answer: Depending on how you implement this, it either won’t work or will be very very inefficient.

![](absolute-embedding-sliding-window-1.png)
![](absolute-embedding-sliding-window-2.png)

> I have a toy input sentence here with a toy language model, whose context size is 4 tokens. We see two subsequent inference passes.

> Let’s look at the token ‘jumped’ in these two subsequent forward passes with the sliding window + absolute embeddings approach. ‘Jumped’ was assigned position 4 in the initial forward pass, and then if we use this sliding window approach we would have to treat ‘jumped’ as position 3 in the next forward pass, even though we need to attend to the old cached representation in which it had position 4. This weirdness that the model definitely didn’t experience during training just leads it to produce very bad predictions. This approach does not work.

