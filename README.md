# Haystack_LLM_pipelines
Pipelines using Haystack Framework


Haystack is an open-source framework by deepset that allows developers to orchestrate LLM applications made up of different components like models, vector DBs, file converters, and countless other modules. Haystack provides pipelines and Agents, helpful in designing LLM applications for various use cases including search, question answering, and conversational AI.

The example uses DocumentStore and Pipeline to do text seaching across a Countries and Capital dataset (from AWS Deepset)

The DocumentStore is used to cache the documents needed to retrieve answers to your questions. This example, uses the InMemoryDocumentStore.

It also uses the BM25 Retriever method for text retrieval.

The prebuilt pipelines created are

- document search (DocumentSearchPipeline),
- document search with summarization (SearchSummarizationPipeline)
- FAQ style QA (FAQPipeline)
- translated search (TranslationWrapperPipeline)

The first pipeline created is based on the BM25 retriever a keyword based retriever

<img width="158" alt="image" src="https://github.com/amarjit420/Haystack_LLM_pipelines/assets/80757241/75e63bd5-af6d-4f28-aa5b-40a05461cb79">

Pipelines can be created and merged, the example uses the  `EmbeddingRetriever` with the keyword based `BM25Retriever`.

Using the `JoinDocuments` node to merge the predictions from each retriever:

![image](https://github.com/deepset-ai/haystack/blob/main/docs/img/tutorial11_custompipelines_pipeline_ensemble.png?raw=true)

