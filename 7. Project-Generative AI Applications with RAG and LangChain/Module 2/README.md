# Embed documents using watsonx's embedding model

### Introduction to document embedding
In the realm of natural language processing (NLP), document embedding refers to the process of converting textual documents into numerical vectors. These vectors capture the semantic meaning of the documents, enabling machines to understand and process human language. Embedding models play a crucial role in this transformation, serving as the backbone for numerous NLP tasks, such as text classification, sentiment analysis, and information retrieval.

### Understanding watsonx's embedding model
IBM's watsonx.ai offers powerful embedding models tailored to meet the demands of modern NLP applications. You can find more information [here](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/fm-models-embed.html?utm_source=skills_network&utm_content=in_lab_content_link&utm_id=Lab-Reading%3A+Embed+documents+using+watsonx%E2%80%99s+embedding+model_v1_1724329919&context=wx). These models excel at creating high-quality embeddings that can capture the nuances of language across various contexts.

### Steps to embed documents using models from watsonx.ai
1. **Preparation of data**:
* Ensure that your documents are clean and preprocessed. This involves tasks like removing special characters, normalizing text, and tokenization.
* Organize your documents into a format that is compatible with model's input requirements, typically as a list of strings or a data set.

2. **Loading the watsonx embedding model**:
* Access embedding models through watsonx.ai's API or platform interface. You will learn how to do it in the corresponding hands-on lab.
* Load the pretrained embedding model, which is optimized for generating document embeddings.

3. **Embedding process**:
* Pass the prepared documents through the embedding model.
* The model will convert each document into a fixed-size numerical vector. These vectors are dense and capture the semantic meaning of the documents.

4. **Postprocessing**:
* After obtaining the embeddings, consider normalizing the vectors if necessary.
* Store the embeddings in a suitable format, such as a database, for further use in downstream tasks.

### Applications of document embeddings
1. **Document clustering**:
* Use the embeddings to group similar documents together. This is particularly useful in organizing large document collections or creating topic-based clusters.

2. **Semantic search**:
* Implement a semantic search engine where queries are matched with documents based on their semantic similarity rather than just keyword matching.

3. **Text classification**:
* Utilize the embeddings as input features for classification models to categorize documents into predefined labels.

### Benefits of using watsonx's embedding model
* **High accuracy**: watsonx's model is designed to produce embeddings that accurately reflect the semantic content of documents, leading to better performance in NLP tasks.
* **Scalability**: The model can handle large data sets efficiently, making it suitable for enterprise-level applications.
* **Versatility**: The embeddings can be applied to a variety of use cases, from search engines to recommendation systems.

### Challenges and considerations
* **Computational resources**: Embedding large volumes of documents requires substantial computational power, especially for real-time applications.
* **Model interpretability**: While embeddings are powerful, they can be difficult to interpret directly, as the vector representation is abstract and not human-readable.

# Compare Fine-Tuning Using InstructLab with RAG

### Introduction
In the ever-evolving field of natural language processing (NLP), extracting relevant information from large sets of documents is a common challenge. Two prominent methods to tackle this issue are fine-tuning a model and retrieval-augmented generation (RAG). Both approaches aim to improve the accuracy and relevance of the information retrieved from documents, but they operate in fundamentally different ways.

### 1. What is fine-tuning?
Fine-tuning involves taking a pre-trained language model (like BERT, GPT, etc.) and training it further on a specific dataset or task. The idea is to adapt the model's knowledge to better suit the nuances of the target domain.

* **How it works**: During fine-tuning, the model's weights are updated based on the specific training data, allowing it to specialize in certain types of tasks or domains, such as sentiment analysis, entity recognition, or document classification.
* **Example use case**: Suppose you have a large corpus of medical documents. By fine-tuning a pre-trained model on this corpus, you can create a model that is better at understanding and retrieving relevant medical information.

IBM created a library called [InstructLab](https://github.com/instructlab), which allows for the easy fine-tuning of LLMs on your local machine, including on laptops. InstructLab is capable of fine-tuning models in order to impart the model with new knowledge, or to impart it with a new set of skills. Moreover, InstructLab provides a structured way of separating different pieces of knowledge and skill using a taxonomy which allows for the easy augmentation and updating of the information on which one would like to fine-tune the model.

### 2. What is RAG?
RAG is an innovative approach that combines the strengths of information retrieval and generative models. Instead of relying solely on the model's pre-trained knowledge, RAG integrates an external knowledge base (such as a document index) to retrieve relevant information dynamically and then uses this information to generate a response.

* **How it works**: When a query is posed, RAG first retrieves the most relevant documents from the knowledge base. Then, it uses these retrieved documents as context to generate a more accurate and informed response using a generative model.
* **Example use case**: In the same medical document scenario, RAG would retrieve the most relevant documents in response to a query and then generate an answer based on this up-to-date and specific information.

### 3. Key differences and trade-offs

| **Aspect** |	**Fine-tuning** |	**RAG** |
| ---------- | ---------------- | ------- |
| **Model training** |	Requires extensive training on the specific domain data. |	Minimal training required; relies on a pre-trained model and an external knowledge base. |
|**Adaptability** |	Highly specialized for a particular domain once trained. |	More flexible, as it can retrieve information from various domains without retraining. |
| **Knowledge updating** |	Updating knowledge requires re-training or fine-tuning the model on new data. |	Knowledge base can be updated independently of the model, allowing for more dynamic responses. |
| **Resource requirements** |	Requires significant computational resources for fine-tuning, especially with large models. |	Lower computational cost as the heavy lifting is done by the retrieval step. |
| **Accuracy and relevance** |	High accuracy in the domain it's trained on but may struggle with out-of-domain queries. |	High relevance, especially in domains with large, dynamic knowledge bases. |
| **Use cases** |	Ideal for tasks with well-defined, static knowledge requirements.	| Ideal for tasks where information is constantly evolving or when dealing with broad domains.|

### 4. When to use fine-tuning vs. RAG
* **Fine-tuning** is suitable when you have a well-defined domain with specific tasks and a stable knowledge base. It excels in environments where precision and specialized knowledge are paramount.
* **RAG** is the preferred choice when you need to handle queries across a broad or dynamic knowledge base, especially when the information is frequently updated or when you require a more general-purpose model.

### 5. Conclusion
Both fine-tuning and RAG offer powerful tools for retrieving information from documents, but they are best suited for different scenarios. Fine-tuning is ideal for specialized, domain-specific tasks, while RAG shines in environments where information is constantly changing or needs to be pulled from diverse sources. By understanding the strengths and limitations of each approach, you can choose the method that best aligns with your specific requirements.

# Module Summary: RAG Using LangChain

Congratulations! You have completed this module. At this point in the course, you know: 

* LangChain uses text splitters to split a long document into smaller chunks.
* Text splitters operate along two axes: Method used to break the text and how the chunk is measured.
* Key parameters of a text splitter: Separator, chunk size, chunk overlap, and length function.
* Commonly used splitters: Split by Character, Recursively Split by Character, Split Code, and Markdown Header Text Splitter.
* Embeddings from data sources can be stored using a vector store.
* A vector database retrieves information based on queries using similarity search.
* Chroma DB is a vector store supported by LangChain that saves embeddings along with metadata.
* To construct the Chroma DB vector database, import the Chroma class from LangChain vector stores and call the chunks and embedding model.
* A similarity search process starts with a query, which the embedding model converts into a numerical vector format.
* The vector database compares the query vector to all the vectors in its storage to find the ones most similar to the query.
* A LangChain retriever is an interface that returns documents based on an unstructured query.
* Vector Store-Based Retriever retrieves documents from a vector database using similarity search or MMR.
* Similarity search is when the retriever accepts a query and retrieves the most similar data.
* MMR is a technique used to balance the relevance and diversity of retrieved results.
