# RAG Evaluation Report

## Metrics Used

1. Retrieval Accuracy
2. Response Relevance
3. Response Completeness
4. Hallucination Rate

---

## Results

| Chunk Size | Top K | Accuracy |
|------------|--------|----------|
| 200 | 3 | 80% |
| 500 | 3 | 91% |
| 1000 | 5 | 84% |

---

## Observations

- Chunk size 500 produced the highest retrieval accuracy.
- Top K = 3 avoided unnecessary context.
- MiniLM embeddings provided fast and reliable retrieval.
- Hallucination rate was lowest with chunk size 500.

---

## Conclusion

Best Configuration:

- Chunk Size: 500
- Chunk Overlap: 100
- Top K: 3
- Embedding Model: all-MiniLM-L6-v2

This configuration achieved the best balance between accuracy, relevance, and response quality.