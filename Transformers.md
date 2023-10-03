Type: #source 
References: https://txt.cohere.ai/what-are-transformer-models/

Transformers have four major parts:
1) Tokenization
2) Embedding
3) Positional Encoding
4) Transforming Block
5) Softmax

1) Tokenization. 
	This step just converts every word or punctuation mark to a corresponding token.
2) Embedding
	Each word is converted into a vector. Words that are similar will have similar vectors (i.e. coordinates).
3) Positional Encoding
	The vectors are combined in a way that preserves the order of each word.
4) Transformer block
	A feedforward neural network is then used to predict the next word in the sentence. An attention component is combined with each NN to form each transformer block. The transfomer concatenates each individual transformer block. 
	
	Attention - this gives context to every word based on other words in the sentence or text. Words that give context to each other are pushed together in the embedding. 

5) Softmax
	This layers takes scores that come from the transfomer block and converts them to probabilities. The highest probability is used to determine the next word.  