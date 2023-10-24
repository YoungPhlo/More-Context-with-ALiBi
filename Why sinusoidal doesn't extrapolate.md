-
![](https://twitter.com/OfirPress/status/1435690039925567489)

> I first tried enabling extrapolation from 1k to 2k tokens by training on 1k tokens, with sinusoidal embs, but with the first token’s position embedding being drawn from between 1 to 1k. So the model would train on positions 389 to 1388 once and then on 845 to 1844, and so on

> During inference, this model would be able to slightly extrapolate and achieve good results if you gave it position embeddings 200 to 1199, but as soon as you moved to the edges of the 0 to 2k range, performance would drastically degrade.

> So for example, perplexity for the same token sequence, using position embeddings 1 to 1000 would be much worse than it was when using position embeddings 200 to 1199.

> The sampling process used (during training) made it more probable for the model to see position embeddings around 1000 while the positions close to 0 or 2k were observed less. During inference it did well around the center- which means it was overfitting to the positions it saw during training and not understanding the actual concept of positioning.

>There’s more experimental evidence: a 247M param. sinusoidal model is able to extrapolate to 70 tokens more than it saw during training but a 1.3B param. sinusoidal model can’t extrapolate to even 1 token more than its train length. Bigger model => more overfitting.

> The bigger model seems to totally break down when it sees a position embedding that’s just one position away from what it saw during training. To me that shows that the model doesn’t actually understand the concept of positioning.

> I think it just remembers that if 'thank' is at 3 and 'you' is at 4 then that's a phrase and if 'thank' is at 8 and 'you' is at 9 then that's a different phrase. My intuition is that it associates memories with specific absolute embs and doesn't understand relative distance

> With ALiBi, we don’t use any position embeddings and so the model can’t do that overfitting. Instead we just bias the attention in a way that does allow the model to handle sequences much longer than it ever saw in training.
