Task 8: Build an LLM Foundation Report

1. How ChatGPT Understands a Question
When a user enters a question into ChatGPT, the model does not actually "understand" language in the same way humans do. Instead, it processes text through a series of mathematical operations that allow it to identify patterns, relationships, and contextual information learned during training.
The process begins when the user types a sentence.
Example Question
"What are the benefits of Artificial Intelligence?"
Before the model can process this question, it must convert the text into a format that computers can understand.
________________________________________
Step 1: Tokenization
Computers cannot directly understand words or sentences. Therefore, the input text is broken into smaller units called tokens.
For example:
Input:
"What are the benefits of Artificial Intelligence?"
Possible Tokens:
	What 
	are 
	the 
	benefits 
	of 
	Artificial 
	Intelligence 
	? 
Each token is assigned a unique numerical identifier.
Example:
Token	Token ID
What	101
are	205
benefits	320
Artificial	876
Intelligence	945
The exact token IDs vary depending on the tokenizer being used.
________________________________________
Step 2: Converting Tokens into Embeddings
After tokenization, each token is transformed into a numerical vector called an embedding.
Instead of treating words as simple numbers, embeddings represent words in a high-dimensional mathematical space.
For example:
Artificial → [0.12, 0.56, -0.31, ...]
Intelligence → [0.87, -0.22, 0.45, ...]
These vectors may contain hundreds or thousands of dimensions.
Embeddings allow the model to capture semantic relationships between words.
________________________________________
Step 3: Context Processing
The model then analyzes how words relate to each other within the sentence.
For example:
"What are the benefits of Artificial Intelligence?"
The model identifies:
	Main topic: Artificial Intelligence 
	Intent: Request for information 
	Focus: Benefits 
This is achieved through attention mechanisms inside the transformer architecture.
________________________________________
Step 4: Building Internal Representations
As the sentence passes through multiple transformer layers, the model creates increasingly rich representations of the input.
At lower layers:
	Grammar is identified 
	Word relationships are detected 
At higher layers:
	Meaning is extracted 
	User intent is inferred 
	Relevant knowledge is activated 
________________________________________
Step 5: Generating a Response
Once the question is processed, the model predicts the most appropriate sequence of words to answer the user's query.
The response is generated one token at a time until a complete answer is formed.
________________________________________
2. How Embeddings Represent Meaning
Embeddings are one of the most important innovations in modern NLP.
They convert words, phrases, sentences, and documents into numerical vectors that preserve meaning.
________________________________________
Traditional Representation
Early NLP systems used one-hot encoding.
Example vocabulary:
	Cat 
	Dog 
	Car 
Representations:
Cat = [1,0,0]
Dog = [0,1,0]
Car = [0,0,1]
Problem:
The model sees no relationship between "Cat" and "Dog."
________________________________________
Embedding Representation
Embeddings solve this issue.
Example:
Cat = [0.82, 0.45, 0.11]
Dog = [0.79, 0.48, 0.10]
Car = [0.05, 0.88, 0.91]
Notice:
	Cat and Dog vectors are similar. 
	Car is located elsewhere. 
This means the model understands that cats and dogs are related concepts.
________________________________________
Semantic Meaning
Words with similar meanings appear closer together in vector space.
Examples:
	King 
	Queen 
	Prince 
	Princess 
These words occupy nearby regions.
Similarly:
	Happy 
	Joyful 
	Excited 
cluster together.
________________________________________
Sentence Embeddings
Entire sentences can also be converted into embeddings.
Sentence A:
"AI is changing the world."
Sentence B:
"Artificial Intelligence is transforming industries."
These sentences have similar meanings.
Therefore, their embeddings are close together.
Sentence C:
"I enjoy playing cricket."
This sentence discusses a completely different topic.
Its embedding will be farther away.
________________________________________
Why Embeddings Are Important
Embeddings enable:
	Semantic search 
	Recommendation systems 
	Question answering 
	Chatbots 
	Information retrieval 
	Retrieval-Augmented Generation (RAG) 
Without embeddings, modern AI systems would struggle to understand meaning.
________________________________________
3. How Attention Helps Models Understand Context
Attention is the core innovation behind transformers.
It allows the model to focus on the most relevant words when processing language.
________________________________________
The Context Problem
Consider the sentence:
"The animal didn't cross the road because it was tired."
What does "it" refer to?
Possibilities:
	Animal 
	Road 
Humans instantly know "it" refers to the animal.
Traditional NLP systems often struggled with such references.
________________________________________
Self-Attention
Self-attention enables every word to examine every other word in the sentence.
The word "it" can look back and determine that "animal" is the most relevant reference.
This helps the model understand context more effectively.
________________________________________
Query, Key, and Value
Each token produces:
	Query (Q) 
	Key (K) 
	Value (V) 
These vectors determine how strongly tokens interact.
The attention score is calculated using:
Attention(Q,K,V)=softmax((QK^T)/√(d_k ))V
The resulting scores indicate which words deserve more focus.
________________________________________
Example
Sentence:
"The doctor told the patient that she should rest."
The word "she" may refer to:
	Doctor 
	Patient 
Attention mechanisms evaluate surrounding context to determine the most likely reference.
________________________________________
Multi-Head Attention
Transformers use multiple attention heads.
Each head focuses on different relationships.
One head may analyze:
	Grammar 
Another may analyze:
	Subject-object relationships 
Another may analyze:
	Long-distance dependencies 
Combining these perspectives improves understanding.
________________________________________
Benefits of Attention
Better Context Understanding
The model considers the entire sentence simultaneously.
Long-Range Dependencies
Words separated by many tokens can still influence one another.
Parallel Processing
All tokens are processed at once.
This significantly speeds up training.
________________________________________
4. Why Transformers Replaced RNNs
Before transformers, Recurrent Neural Networks (RNNs) dominated NLP.
Variants included:
	RNN 
	LSTM 
	GRU 
Although revolutionary at the time, they had major limitations.
________________________________________
How RNNs Work
RNNs process text sequentially.
Example:
Word1 → Word2 → Word3 → Word4
Each word depends on previous computations.
This prevents parallelization.
________________________________________
Problem 1: Slow Training
Because words are processed one at a time, training becomes slow.
For long documents:
	Processing time increases significantly. 
Transformers solve this by processing all tokens simultaneously.
________________________________________
Problem 2: Vanishing Gradients
As sequences become longer, information from earlier words can fade.
Example:
"The student who studied for months and completed many projects before the final examination passed."
The model may forget important earlier information.
________________________________________
Problem 3: Limited Context
RNNs struggle to connect distant words.
Long-range relationships become difficult to learn.
________________________________________
Transformer Advantages
Parallel Processing
Entire sequences are processed simultaneously.
Better Context Handling
Attention allows any token to interact with any other token.
Scalability
Models can be trained on massive datasets.
Improved Accuracy
Transformers consistently outperform RNNs.
________________________________________
Comparison
Feature	RNN	Transformer
Sequential Processing	Yes	No
Parallel Processing	No	Yes
Long Context Handling	Weak	Strong
Training Speed	Slow	Fast
Scalability	Limited	Excellent
Performance	Moderate	Superior
Because of these advantages, transformers became the foundation of modern LLMs.
________________________________________
5. How LLMs Generate the Next Word
Text generation is fundamentally a prediction problem.
The model predicts the most likely next token based on previous tokens.
________________________________________
Example
Input:
"The sky is"
Possible next tokens:
Token	Probability
blue	70%
clear	15%
bright	10%
dark	5%
The model selects one token based on these probabilities.
________________________________________
Step-by-Step Generation
Step 1
Input:
"The sky is"
Step 2
Model predicts:
"blue"
Sentence becomes:
"The sky is blue"
Step 3
New input:
"The sky is blue"
Model predicts:
"today"
Sentence becomes:
"The sky is blue today"
Step 4
Continue until completion.
________________________________________
Probability Distribution
At each step, the model calculates probabilities for every token in its vocabulary.
Modern vocabularies may contain:
	50,000 tokens 
	100,000 tokens 
	More than 250,000 tokens 
The model chooses the next token based on these probabilities.
________________________________________
Temperature
Temperature controls creativity.
Low Temperature
Produces predictable responses.
Example:
"The capital of France is Paris."
High Temperature
Produces more diverse outputs.
Example:
"The future of AI may unfold through unexpected collaborations between humans and intelligent systems."
________________________________________
Autoregressive Generation
Most modern LLMs generate text autoregressively.
This means:
	Predict next token. 
	Append token. 
	Use updated sequence. 
	Predict again. 
Repeat until complete.
________________________________________
Training Objective
During training, the model learns by predicting missing words.
Example:
Input:
"Artificial Intelligence is ___"
Expected:
"transforming"
If the prediction is incorrect:
	Error is calculated. 
	Model weights are adjusted. 
	Learning occurs. 
After billions of examples, the model becomes highly effective at predicting language patterns.
