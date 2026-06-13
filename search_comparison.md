Task 7: Traditional Search vs Semantic Search
Traditional Search
Uses keyword matching.
Example:
Query: car
Matches documents containing "car".
Advantages
•	Fast 
•	Simple 
Limitations
•	Misses synonyms 
•	Limited understanding 

________________________________________
Semantic Search
Uses embeddings.
Example
Query:automobile
Can retrieve documents containing:
car
vehicle
transportation
even without exact keyword matching.
________________________________________
Why Embeddings Changed NLP
Embeddings convert language into numerical representations that preserve semantic relationships.
Benefits
•	Similar meanings cluster together. 
•	Improved retrieval quality. 
•	Better recommendations. 
________________________________________
Importance in RAG
Retrieval-Augmented Generation (RAG) relies on semantic search.
Workflow
User Query
    |
Embedding
    |
Vector Database
    |
Relevant Documents
    |
LLM Response
Without embeddings, RAG cannot retrieve semantically relevant information.
________________________________________
Vector Databases
Examples:
•	Pinecone 
•	Weaviate 
•	Milvus 
•	Qdrant 
Purpose:
•	Store embeddings 
•	Fast similarity search 
•	Power AI applications
