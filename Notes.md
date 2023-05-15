The main advantage in comparison to using "just" LLM is the presense of **VectorStore**.
General pipeline: 
- Relevant documents are vectorised to a VectorStore
- User sends a request/question to both LLM and VectorStore simultaneously
- The request is vectorized and used for similarity search in VectorStore. Based on similarity, the corresponding action/document is fetched from VectorStore and fed to the LLM as well. This way, LLM has now two inputs: from the initial request and from VectorStore, hence it can provide an answer or action.
In this way, these applications are data-aware (due to referencing our own data in VectorSore, i.e. DB schema, Customer/Marketing data etc.) and they are agentic (are able to conduct actions)