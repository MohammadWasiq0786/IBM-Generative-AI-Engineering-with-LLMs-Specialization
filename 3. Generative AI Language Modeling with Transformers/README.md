# Course Conclusion

Congratulations! You've successfully completed the course and are now equipped with valuable insights into the transformative world of natural language processing (NLP) using transformer-based models. At this point, you know that:

* Positional encoding incorporates information about the position of each embedding within a sequence.
* Segment embeddings are related to positional encodings, providing additional positional information. 
* Attention mechanisms employ query, key, and value matrices.
* To employ attention for sequences, you can consolidate all the query vectors into a single matrix.
* Simple language modeling in the self-attention mechanism predicts the following word in the sentence.
* Self-attention mechanisms help generate output using various methods.
* The scaled dot-product attention mechanism involves a series of matrix multiplications that incorporate queries, keys, and a scaling factor. A masking operation may be employed, and the values are multiplied to produce the output.

* To create the text pipeline:
> * Create iterators, allocate training sets, generate tokens, and construct vocabulary. 
> * Design a custom collate function, apply padding, and create a data loader. 

* To create the model:
> * Instantiate the embedding layer, add positional encoding, and apply the transformer encoder layers.
> * Use the classifier layer to predict the label to which the input text belongs.

* To train the model:
> * Use the same process as a standard classification problem.

* The decoder employs actual word embeddings rather than their approximations throughout the training.
* To predict the decoder model for the next token, specify the context size and randomly select a point in the sequence. 
* Custom GPT model architecture helps create a decoder model to predict the next token.

* BERT’s architecture allows for fine-tuning specific tasks like: 
> * Text summarization 
> * Question answering 
> * Sentiment analysis

* BERT utilizes an encoder-only architecture to process entire sequences of text simultaneously.

* In the NSP task
> * Input consists of word embeddings processed by the encoder to generate contextual embeddings. 
> * Contextual embeddings determine if the second sentence logically follows the first.

* The linear layer generates the output vectors, the predictions the model returns.
* Transformers process the entire text sequence simultaneously for language translation.
* Cross-attention computes attention scores between each target position and all source positions.

## Important Links

* [**PyTorch**](https://pytorch.org/)
* [**IBM NLP**](https://www.ibm.com/topics/natural-language-processing)
* [**Transformer**](https://www.ibm.com/topics/transformer-model)
* [**Gen AI Blog**](https://research.ibm.com/blog/time-series-AI-transformers)
