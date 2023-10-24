---
annotation-target: pdf/train_short_test_long_alibi.pdf
---

>%%
>```annotation-json
>{"text":"**Estimation** at inference time\n\nIn mathematics, extrapolation is a type of estimation, beyond the original observation range, of the value of a variable on the basis of its relationship with another variable.\n\nIt is the extension of a graph, curve, or range of values by inferring unknown values from trends in the known data.","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":474,"end":505},{"type":"TextQuoteSelector","exact":" extrapolationat inference time","prefix":"swered: how does a model achieve","suffix":"for sequences that are longer t"}]}],"created":"2023-08-07T11:13:00.291Z","updated":"2023-08-07T11:13:00.291Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%swered: how does a model achieve%%HIGHLIGHT%% ==extrapolationat inference time== %%POSTFIX%%for sequences that are longer t*
>%%LINK%%[[#^hbcnmh0xx0t|show annotation]]
>%%COMMENT%%
>**Estimation** at inference time
>
>In mathematics, extrapolation is a type of estimation, beyond the original observation range, of the value of a variable on the basis of its relationship with another variable.
>
>It is the extension of a graph, curve, or range of values by inferring unknown values from trends in the known data.
>%%TAGS%%
>
^hbcnmh0xx0t


>%%
>```annotation-json
>{"text":"One way to help the model understand longer texts is by changing the way it keeps track of the positions of words in the text. We use page numbers or chapters to keep track of where we are in a book, the model uses something called \"position representations\" to know the order of words in a sentence.\n\n**Question:** What position representation method did they change from?","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":622,"end":666},{"type":"TextQuoteSelector","exact":"changing the position represen-tation method","prefix":"lation can be enabled by simply","suffix":", though we find that current me"}]}],"created":"2023-08-07T11:18:48.221Z","updated":"2023-08-07T11:18:48.221Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%lation can be enabled by simply%%HIGHLIGHT%% ==changing the position represen-tation method== %%POSTFIX%%, though we find that current me*
>%%LINK%%[[#^ma6v3ei9ym|show annotation]]
>%%COMMENT%%
>One way to help the model understand longer texts is by changing the way it keeps track of the positions of words in the text. We use page numbers or chapters to keep track of where we are in a book, the model uses something called "position representations" to know the order of words in a sentence.
>
>**Question:** What position representation method did they change from?
>%%TAGS%%
>
^ma6v3ei9ym


>%%
>```annotation-json
>{"text":"Positional embeddings are **markers that help the model understand the order of words** in a sentence.\n\nALiBi doesn't directly add any extra information to the words themselves to show their positions in the sentence.","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":854,"end":911},{"type":"TextQuoteSelector","exact":"LiBi does not add positional embeddingsto word embeddings","prefix":"on with Linear Biases (ALiBi). A","suffix":"; instead, it biases query-key a"}]}],"created":"2023-08-07T11:18:56.882Z","updated":"2023-08-07T11:18:56.882Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%on with Linear Biases (ALiBi). A%%HIGHLIGHT%% ==LiBi does not add positional embeddingsto word embeddings== %%POSTFIX%%; instead, it biases query-key a*
>%%LINK%%[[#^5o6urlh6tps|show annotation]]
>%%COMMENT%%
>Positional embeddings are **markers that help the model understand the order of words** in a sentence.
>
>ALiBi doesn't directly add any extra information to the words themselves to show their positions in the sentence.
>%%TAGS%%
>
^5o6urlh6tps


>%%
>```annotation-json
>{"text":"Attention is the model's way of focusing on different parts of the input text. ALiBi adjusts how much attention the model gives to different words based on how far apart they are from each other in the sentence. \n\nThis bias is like a \"penalty\" that makes the model focus on the relationships that matter the most for understanding the context of the sentence.","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":925,"end":1011},{"type":"TextQuoteSelector","exact":"biases query-key attention scores with a penaltythat is proportional to their distance","prefix":"to word embeddings; instead, it","suffix":". We show that this method train"}]}],"created":"2023-08-07T11:19:07.981Z","updated":"2023-08-07T11:19:07.981Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%to word embeddings; instead, it%%HIGHLIGHT%% ==biases query-key attention scores with a penaltythat is proportional to their distance== %%POSTFIX%%. We show that this method train*
>%%LINK%%[[#^9ur553imt5|show annotation]]
>%%COMMENT%%
>Attention is the model's way of focusing on different parts of the input text. ALiBi adjusts how much attention the model gives to different words based on how far apart they are from each other in the sentence. 
>
>This bias is like a "penalty" that makes the model focus on the relationships that matter the most for understanding the context of the sentence.
>%%TAGS%%
>
^9ur553imt5


>%%
>```annotation-json
>{"text":"A technique used in the transformer model to help it understand the order or position of words in a sequence.\n\nInstead of using specific markers or flags to show the position of each word, the model adds special values to the word embeddings. These special values are **patterns that repeat in a sinusoidal (wave-like) manner**.\n\nThese sinusoidal position embeddings act like a map that helps the model figure out where each word is located in the sequence.","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":1197,"end":1231},{"type":"TextQuoteSelector","exact":"sinusoidal positionembedding model","prefix":"ieving the same perplexity as a","suffix":"trained on inputs of length 204"}]}],"created":"2023-08-07T11:21:11.940Z","updated":"2023-08-07T11:21:11.940Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%ieving the same perplexity as a%%HIGHLIGHT%% ==sinusoidal positionembedding model== %%POSTFIX%%trained on inputs of length 204*
>%%LINK%%[[#^ukkn2ytalsb|show annotation]]
>%%COMMENT%%
>A technique used in the transformer model to help it understand the order or position of words in a sequence.
>
>Instead of using specific markers or flags to show the position of each word, the model adds special values to the word embeddings. These special values are **patterns that repeat in a sinusoidal (wave-like) manner**.
>
>These sinusoidal position embeddings act like a map that helps the model figure out where each word is located in the sequence.
>%%TAGS%%
>
^ukkn2ytalsb


>%%
>```annotation-json
>{"text":"The ALiBi method is designed to **prioritize understanding recent information more effectively**. Give more importance to recent or nearby words in a sequence.\n\nInductive reasoning is starting with specific observations to draw general conclusions versus deductive reasoning where you go from general ideas to specific conclusions.","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":1315,"end":1353},{"type":"TextQuoteSelector","exact":"ALiBi’s inductive bias towards recency","prefix":"aster andusing 11% less memory.","suffix":"also leads it tooutperform mult"}]}],"created":"2023-08-07T11:21:27.124Z","updated":"2023-08-07T11:21:27.124Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%aster andusing 11% less memory.%%HIGHLIGHT%% ==ALiBi’s inductive bias towards recency== %%POSTFIX%%also leads it tooutperform mult*
>%%LINK%%[[#^n5u5390oafm|show annotation]]
>%%COMMENT%%
>The ALiBi method is designed to **prioritize understanding recent information more effectively**. Give more importance to recent or nearby words in a sequence.
>
>Inductive reasoning is starting with specific observations to draw general conclusions versus deductive reasoning where you go from general ideas to specific conclusions.
>%%TAGS%%
>
^n5u5390oafm


>%%
>```annotation-json
>{"text":"This dataset is a collection of over 100 million tokens extracted from the set of verified 'Good' and 'Featured' articles on Wikipedia","target":[{"source":"vault:/pdfs/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":1421,"end":1433},{"type":"TextQuoteSelector","exact":"WikiText-103","prefix":"strong position methods on the","suffix":"benchmark.11 INTRODUCTIONWhen c"}]}],"created":"2023-08-07T11:21:42.489Z","updated":"2023-08-07T11:21:42.489Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdfs/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdfs/train_short_test_long_alibi.pdf"}
>```
>%%
>*%%PREFIX%%strong position methods on the%%HIGHLIGHT%% ==WikiText-103== %%POSTFIX%%benchmark.11 INTRODUCTIONWhen c*
>%%LINK%%[[#^z7f4qaa58|show annotation]]
>%%COMMENT%%
>This dataset is a collection of over 100 million tokens extracted from the set of verified 'Good' and 'Featured' articles on Wikipedia
>%%TAGS%%
>
^z7f4qaa58



>%%
>```annotation-json
>{"created":"2023-08-09T09:02:22.747Z","text":"**Recurrent Neural Networks**: a type of neural network architecture that has the ability to process sequences of data, which makes it suitable for working with language data where the order of words matters.\n\nRNN-based models were trained on sequences of words, and they were typically designed to understand patterns within shorter sequences of words. They were expected to generalize their understanding even though they were trained on shorter sequences.","updated":"2023-08-09T09:02:22.747Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdf/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdf/train_short_test_long_alibi.pdf","target":[{"source":"vault:/pdf/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":1811,"end":1830},{"type":"TextQuoteSelector","exact":"RNN language models","prefix":" train on.2Before transformers, ","suffix":" were trained on shorter-L seque"}]}]}
>```
>%%
>*%%PREFIX%%train on.2Before transformers,%%HIGHLIGHT%% ==RNN language models== %%POSTFIX%%were trained on shorter-L seque*
>%%LINK%%[[#^q1jwi9aj4g|show annotation]]
>%%COMMENT%%
>**Recurrent Neural Networks**: a type of neural network architecture that has the ability to process sequences of data, which makes it suitable for working with language data where the order of words matters.
>
>RNN-based models were trained on sequences of words, and they were typically designed to understand patterns within shorter sequences of words. They were expected to generalize their understanding even though they were trained on shorter sequences.
>%%TAGS%%
>
^q1jwi9aj4g



>%%
>```annotation-json
>{"created":"2023-08-09T09:52:33.948Z","text":"Imagine you're reading a story and you have a bunch of questions about different parts of the story. (**queries**)\n\nYou start by paying close attention to the parts of the text that are directly related to your questions. (**keys**)\n\nBut as you move away from the parts that are most relevant, you might not pay as much attention. The farther you go from your main questions, the less focused you become.","updated":"2023-08-09T09:52:33.948Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdf/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdf/train_short_test_long_alibi.pdf","target":[{"source":"vault:/pdf/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":2977,"end":3117},{"type":"TextQuoteSelector","exact":"ALiBi negatively biases attention scores with a linearly decreasing penalty proportional to the dis-tance between the relevant key and query","prefix":"ilitate efficient extrapolation.","suffix":". Our simple approach eliminates"}]}]}
>```
>%%
>*%%PREFIX%%ilitate efficient extrapolation.%%HIGHLIGHT%% ==ALiBi negatively biases attention scores with a linearly decreasing penalty proportional to the dis-tance between the relevant key and query== %%POSTFIX%%. Our simple approach eliminates*
>%%LINK%%[[#^qqbrw8fv1of|show annotation]]
>%%COMMENT%%
>Imagine you're reading a story and you have a bunch of questions about different parts of the story. (**queries**)
>
>You start by paying close attention to the parts of the text that are directly related to your questions. (**keys**)
>
>But as you move away from the parts that are most relevant, you might not pay as much attention. The farther you go from your main questions, the less focused you become.
>%%TAGS%%
>
^qqbrw8fv1of


>%%
>```annotation-json
>{"created":"2023-08-09T10:07:11.087Z","text":"In a nutshell, the perplexity of a language model measures the degree of uncertainty of a LM when it generates a new token, averaged over very long sequences.\n\nA lower perplexity value indicates that the model is better at predicting the next word and understanding the sequence of words.","updated":"2023-08-09T10:07:11.087Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdf/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdf/train_short_test_long_alibi.pdf","target":[{"source":"vault:/pdf/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":3854,"end":3865},{"type":"TextQuoteSelector","exact":"perplexity ","prefix":", rotary, and T5) show degraded ","suffix":"(y-axis, lower is better), butou"}]}]}
>```
>%%
>*%%PREFIX%%, rotary, and T5) show degraded%%HIGHLIGHT%% ==perplexity== %%POSTFIX%%(y-axis, lower is better), butou*
>%%LINK%%[[#^hjxcf995b7k|show annotation]]
>%%COMMENT%%
>In a nutshell, the perplexity of a language model measures the degree of uncertainty of a LM when it generates a new token, averaged over very long sequences.
>
>A lower perplexity value indicates that the model is better at predicting the next word and understanding the sequence of words.
>%%TAGS%%
>
^hjxcf995b7k



>%%
>```annotation-json
>{"created":"2023-08-09T11:28:08.607Z","text":"The key/value/query concept is analogous to retrieval systems. For example, when you search for videos on Youtube, the search engine will map your **query** (text in the search bar) against a set of **keys** (video title, description, etc.) associated with candidate videos in their database, then present you the best matched videos (**values**).","updated":"2023-08-09T11:28:08.607Z","document":{"title":"train_short_test_long_alibi.pdf","link":[{"href":"urn:x-pdf:7f29a8e689931ed9c60404ec08a38226"},{"href":"vault:/pdf/train_short_test_long_alibi.pdf"}],"documentFingerprint":"7f29a8e689931ed9c60404ec08a38226"},"uri":"vault:/pdf/train_short_test_long_alibi.pdf","target":[{"source":"vault:/pdf/train_short_test_long_alibi.pdf","selector":[{"type":"TextPositionSelector","start":3103,"end":3117},{"type":"TextQuoteSelector","exact":" key and query","prefix":"e dis-tance between the relevant","suffix":". Our simple approach eliminates"}]}]}
>```
>%%
>*%%PREFIX%%e dis-tance between the relevant%%HIGHLIGHT%% ==key and query== %%POSTFIX%%. Our simple approach eliminates*
>%%LINK%%[[#^kbrpk8mlow|show annotation]]
>%%COMMENT%%
>The key/value/query concept is analogous to retrieval systems. For example, when you search for videos on Youtube, the search engine will map your **query** (text in the search bar) against a set of **keys** (video title, description, etc.) associated with candidate videos in their database, then present you the best matched videos (**values**).
>%%TAGS%%
>
^kbrpk8mlow
