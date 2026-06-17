Why It Works Best

1. Maintains Context

A chunk size of 500 characters contains enough information to preserve the meaning of a section without breaking important sentences.

2. Better Retrieval Accuracy

When users ask questions, the retrieved chunk usually contains complete information, resulting in more accurate answers.

3. Reduces Information Loss

Using a 100-character overlap ensures that information appearing at chunk boundaries is not lost during retrieval.

4. Balanced Number of Chunks

Smaller chunk sizes create too many chunks, increasing storage and retrieval time. Larger chunk sizes may contain unrelated information. A 500-character chunk provides a good balance.


Conclusion

The 500-character chunk size with 100-character overlap performed best because it preserved context, improved semantic search accuracy, reduced information loss, and generated more relevant responses in the RAG pipeline. This strategy is recommended for most document-based question-answering systems.