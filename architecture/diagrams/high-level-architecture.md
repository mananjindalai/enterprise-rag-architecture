# High-Level Architecture Diagram

```mermaid
graph TD
    A[User Query] --> B[API Gateway]
    B --> C[Query Processing Layer]
    C --> D[Retriever]
    D --> E[Vector Database]
    E --> D
    D --> F[Reranker]
    F --> G[LLM Generation]
    G --> H[Response + Citations]
    H --> I[Evaluation & Observability]
    
    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#e8f5e9
    style D fill:#fce4ec
    style E fill:#f3e5f5
    style F fill:#e0f2f1
    style G fill:#fff3e0
    style H fill:#e8eaf6
    style I fill:#f1f8e9
```

## Components

### API Gateway
- Entry point for all requests
- Authentication and authorization
- Rate limiting
- Request routing

### Query Processing Layer
- Query preprocessing
- Query expansion
- Query transformation
- Multi-query generation

### Retriever
- Vector search
- Hybrid search
- Metadata filtering
- Multi-query retrieval

### Vector Database
- FAISS / Pinecone / Weaviate
- Embedding storage
- Semantic search
- Scalable retrieval

### Reranker
- Cross-encoder reranking
- Context compression
- Relevance scoring
- Result optimization

### LLM Generation
- Context injection
- Prompt engineering
- Response generation
- Citation extraction

### Evaluation & Observability
- Quality metrics
- Performance monitoring
- User feedback
- Continuous evaluation
