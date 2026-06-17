Introduction
Large Language Models (LLMs) such as GPT, Llama, Claude, and Gemini have transformed how organizations interact with information. However, these models suffer from a major limitation: they do not have access to real-time enterprise knowledge unless that information was included during training. This limitation often results in outdated responses, missing information, or hallucinations.
Retrieval-Augmented Generation (RAG) solves this problem by combining information retrieval techniques with generative AI. Instead of relying solely on pre-trained knowledge, RAG retrieves relevant documents from external sources and provides them to the language model before generating a response.
Modern enterprise systems have evolved from simple RAG pipelines to sophisticated Advanced RAG Architectures that include hybrid search, metadata filtering, query expansion, re-ranking, grounding, hallucination prevention, and context compression.
________________________________________
1. Basic RAG
What is Basic RAG?
Retrieval-Augmented Generation (RAG) is an AI architecture that combines:
1.	Information Retrieval 
2.	Large Language Models 
The goal is to provide accurate and context-aware responses using external knowledge sources.
Basic Workflow
User Query
     │
     v
Retriever
     │
     v
Vector Database
     │
     v
Relevant Chunks
     │
     v
  LLM
     │
     v
Generated Answer
Example
User Query:
What is the notice period for employees?
Retriever finds:
Employees must serve a 60-day notice period before resignation.
The LLM generates:
According to company policy, employees are required
to provide a 60-day notice period before resignation.
Advantages
•	Uses external knowledge 
•	Reduces hallucinations 
•	Provides up-to-date information 
•	Easy implementation 
Limitations
•	Retrieval quality affects answers 
•	Poor ranking may retrieve irrelevant documents 
•	Limited understanding of user intent 
•	Large contexts increase token costs 
________________________________________
2. Advanced RAG
Advanced RAG extends the basic pipeline by adding multiple optimization layers.
Advanced Architecture
User Query
      │
      v
Query Expansion
      │
      v
Metadata Filtering
      │
      v
Hybrid Search
      │
      v
Top 20 Documents
      │
      v
Re-ranking
      │
      v
Top 5 Documents
      │
      v
Context Compression
      │
      v
Grounded Prompt
      │
      v
LLM
      │
      v
Hallucination Validation
      │
      v
Answer + Citations
Benefits
•	Higher retrieval accuracy 
•	Better scalability 
•	Stronger security controls 
•	Improved answer quality 
•	Enterprise readiness 
________________________________________
3. Hybrid Search
Why Hybrid Search?
Traditional retrieval systems use either:
Sparse Retrieval
Keyword-based matching.
Example:
Leave Policy
Matches documents containing:
leave
policy
Dense Retrieval
Embedding-based semantic matching.
Example:
Time-off regulations
Can still retrieve:
Employee leave policy
even without exact keywords.
________________________________________
BM25 Search
BM25 is a popular ranking algorithm.
It scores documents based on:
•	Term frequency 
•	Document length 
•	Query relevance 
Formula:
Higher Frequency = Higher Score
Example:
Query: leave policy
Document A:
leave policy leave policy
Higher score.
________________________________________
Embedding Search
Documents are converted into vectors.
Example:
Leave Policy
↓
[0.23, 0.91, 0.45, ...]
Query vectors are compared using cosine similarity.
________________________________________
Hybrid Search Formula
Hybrid Score =
0.7 × Semantic Score
+
0.3 × BM25 Score
Benefits:
•	Captures exact keywords 
•	Captures semantic meaning 
•	Improves recall and precision 
________________________________________
4. Re-ranking
Problem
Initial retrieval often returns partially relevant documents.
Example:
Top Results:
1. Payroll Policy
2. Leave Policy
3. Attendance Rules
Leave Policy should be first.
________________________________________
Solution
Use a Cross Encoder.
Stage 1
Retrieve Top 20 documents.
Stage 2
Cross Encoder evaluates each document against the query.
Stage 3
Sort by relevance.

Benefits
•	Improves precision 
•	Better relevance 
•	Higher answer quality 
________________________________________
5. Context Compression
Problem
LLMs have token limits.
Example:
Retrieved Documents:
50 pages
Sending all content is expensive and inefficient.
________________________________________
Context Compression
Only the most relevant information is retained.
Example:
Original:
10 pages
Compressed:
2 paragraphs
Methods
Extractive Compression
Keep important sentences.
Summarization
Generate concise summaries.
Redundancy Removal
Remove duplicate information.

________________________________________
Benefits
•	Lower costs 
•	Faster responses 
•	Better focus 
________________________________________
6. Metadata Filtering
Metadata describes documents.
Example:
{
 "department":"HR",
 "country":"India",
 "year":"2025"
}
________________________________________
Why Metadata Matters
Without filtering:
Search across 1 million documents
With filtering:
Search only HR documents
from India in 2025
________________________________________
Example
User Query:
Find leave policies from India.
Filter:
Department = HR
Country = India
Result:
Relevant HR policies only

________________________________________
Advantages
•	Faster retrieval 
•	Better accuracy 
•	Security enforcement 
•	Lower computational cost 
________________________________________
7. Query Expansion
Problem
Users often provide short queries.
Example:
leave policy
The system may miss:
vacation rules
time off policy
annual leave
________________________________________
Solution
Expand the query.
Expanded Query:
leave policy
employee leave policy
vacation policy
annual leave
sick leave
holiday rules
________________________________________
Expansion Techniques
Synonym Expansion
WordNet:
leave → vacation
LLM Expansion
The LLM predicts related terms.
Historical Query Expansion
Uses previous user searches.
________________________________________
Benefits
•	Improves recall 
•	Finds more relevant documents 
•	Better semantic understanding 
________________________________________
8. Hallucination Prevention
What is Hallucination?
A hallucination occurs when the LLM generates unsupported information.
Example:
Context:
Notice period = 60 days
LLM Response:
Notice period = 90 days
This is a hallucination.
________________________________________
Causes
•	Missing context 
•	Weak retrieval 
•	Ambiguous prompts 
•	Outdated model knowledge 
________________________________________
Prevention Methods
Strong Retrieval
Retrieve reliable sources.
Source Citations
Every answer includes evidence.
Confidence Scoring
Evaluate answer-context similarity.
Validation Layer
Compare generated answers with retrieved documents.
________________________________________
Example
{
 "confidence":92,
 "grounded":true,
 "sources_found":4
}
________________________________________
9. Grounding Techniques
Grounding means ensuring responses are based on retrieved evidence.
________________________________________
Grounded Prompt
Instead of:
Answer the question.
Use:
Answer ONLY using provided context.
________________________________________
Source-Based Grounding
Example:
Source:
HR_Policy.pdf
Page 12
________________________________________
Retrieval Grounding
Answer must originate from retrieved chunks.
________________________________________

Citation Grounding
Example:
Employees must serve 60 days notice.

(Source: HR_Policy.pdf, Section 4.2)
________________________________________
Benefits
•	Trustworthy answers 
•	Transparency 
•	Regulatory compliance 



                    ADVANCED RAG ARCHITECTURE

                         User Query
                              │
                              ▼
                    Query Expansion Engine
                              │
                              ▼
                     Metadata Filtering
                              │
                              ▼
                      Hybrid Retrieval
                 ┌────────────┴────────────┐
                 ▼                         ▼
          Vector Search              BM25 Search
         (Embeddings)              (Keyword Match)
                 └────────────┬────────────┘
                              ▼
                       Score Fusion
                              ▼
                     Top 20 Candidates
                              ▼
                 Cross Encoder Re-Ranking
                              ▼
                      Top 5 Chunks
                              ▼
                    Context Compression
                              ▼
                     Grounded Prompt
                              ▼
                            LLM
                              ▼
                 Hallucination Detection
                              ▼
                   Answer + Citations