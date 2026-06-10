Neural Network
Definition
A Neural Network is a computational model inspired by the human brain. It consists of interconnected nodes called neurons that process information and learn patterns from data.
The main goal of a neural network is to recognize relationships in data and make predictions or classifications.
Real-World Examples
1.	Face Recognition System
2.	Voice Assistants 
3.	Self-Driving Cars 
4.	Recommendation Systems 
5.	Medical Diagnosis 
6.	Fraud Detection 
7.	Language Translation 
Layers in Neural Networks
Input Layer
The input layer receives data from external sources.
Example:
For Iris Dataset:
•	Sepal Length 
•	Sepal Width 
•	Petal Length 
•	Petal Width 
The input layer contains 4 neurons.
Hidden Layer
Hidden layers perform computations and extract patterns.
Functions:
•	Feature Extraction 
•	Pattern Recognition 
•	Non-linear Learning 
Deep neural networks contain multiple hidden layers.
Output Layer
Produces final prediction.
Examples:
Binary Classification:
•	0 = No 
•	1 = Yes 
Multi-Class Classification:
•	Setosa 
•	Versicolor 
•	Virginica 


Activation Functions
ReLU (Rectified Linear Unit)
Characteristics:
•	Fast computation 
•	Solves vanishing gradient problem 
•	Most commonly used 
Used In:
•	Hidden Layers 
•	CNNs 
•	Deep Neural Networks 
Advantages:
•	Efficient 
•	Simple 
•	Faster convergence 

Sigmoid
Output Range:
0 to 1
Used In:
•	Binary Classification 
•	Output Layers 
Advantages:
•	Probability interpretation 
Disadvantages:
•	Vanishing gradient problem 




Tanh
Output Range:
-1 to 1
Used In:
•	Hidden Layers 
•	Recurrent Neural Networks 
Advantages:
•	Zero-centered outputs 
Disadvantages:
•	Computationally expensive 

Softmax
Output:
Probability distribution.
Used In:
•	Multi-class classification 
•	Final output layer 
Example:
Digit Recognition:
Digit 0 : 0.01
Digit 1 : 0.02
Digit 2 : 0.90
Digit 3 : 0.01
...
Prediction = Digit 2

Training Concepts
Epoch
One complete pass through the training dataset.
Example:
Dataset Size = 10,000 images
Epoch = 1
Model sees all 10,000 images once.

Batch Size
Number of samples processed before updating weights.
Example:
Dataset = 10,000
Batch Size = 100
Updates per Epoch:
10000 / 100 = 100 updates

Learning Rate
Controls how much weights change during training.
Small Learning Rate:
•	Slow training 
•	Better accuracy 
Large Learning Rate:
•	Fast training 
•	May overshoot optimum solution 
Common Values:
0.1
0.01
0.001

Loss Function
Measures prediction error.
Examples:
Binary Crossentropy
Binary Classification
Categorical Crossentropy
Multi-class Classification
Mean Squared Error
Regression Problems
Goal:
Minimize loss.

Optimizer
Updates model weights.
Popular Optimizers:
1.	SGD 
2.	Adam 
3.	RMSProp 
4.	Adagrad 
Adam is most commonly used because it combines speed and stability.

Gradient Descent
Optimization algorithm used to reduce loss.
Steps:
1.	Predict output 
2.	Calculate loss 
3.	Compute gradients 
4.	Update weights 
5.	Repeat 
The neural network gradually learns by reducing errors during training.
Importance of Deep Learning
Deep learning can automatically learn complex features from raw data without manual feature engineering.
Applications include:
•	Computer Vision 
•	Natural Language Processing 
•	Healthcare 
•	Finance 
Neural Network
Definition
A Neural Network is a computational model inspired by the human brain. It consists of interconnected nodes called neurons that process information and learn patterns from data.
The main goal of a neural network is to recognize relationships in data and make predictions or classifications.
Real-World Examples
1.	Face Recognition System
2.	Voice Assistants 
3.	Self-Driving Cars 
4.	Recommendation Systems 
5.	Medical Diagnosis 
6.	Fraud Detection 
7.	Language Translation 
Layers in Neural Networks
Input Layer
The input layer receives data from external sources.
Example:
For Iris Dataset:
•	Sepal Length 
•	Sepal Width 
•	Petal Length 
•	Petal Width 
The input layer contains 4 neurons.
Hidden Layer
Hidden layers perform computations and extract patterns.
Functions:
•	Feature Extraction 
•	Pattern Recognition 
•	Non-linear Learning 
Deep neural networks contain multiple hidden layers.
Output Layer
Produces final prediction.
Examples:
Binary Classification:
•	0 = No 
•	1 = Yes 
Multi-Class Classification:
•	Setosa 
•	Versicolor 
•	Virginica 

Activation Functions
ReLU (Rectified Linear Unit)
Characteristics:
•	Fast computation 
•	Solves vanishing gradient problem 
•	Most commonly used 
Used In:
•	Hidden Layers 
•	CNNs 
•	Deep Neural Networks 
Advantages:
•	Efficient 
•	Simple 
•	Faster convergence 

Sigmoid
Output Range:
0 to 1
Used In:
•	Binary Classification 
•	Output Layers 
Advantages:
•	Probability interpretation 
Disadvantages:
•	Vanishing gradient problem 





Tanh
Output Range:
-1 to 1
Used In:
•	Hidden Layers 
•	Recurrent Neural Networks 
Advantages:
•	Zero-centered outputs 
Disadvantages:
•	Computationally expensive 

Softmax
Output:
Probability distribution.
Used In:
•	Multi-class classification 
•	Final output layer 
Example:
Digit Recognition:
Digit 0 : 0.01
Digit 1 : 0.02
Digit 2 : 0.90
Digit 3 : 0.01
...
Prediction = Digit 2

Training Concepts
Epoch
One complete pass through the training dataset.
Example:
Dataset Size = 10,000 images
Epoch = 1
Model sees all 10,000 images once.

Batch Size
Number of samples processed before updating weights.
Example:
Dataset = 10,000
Batch Size = 100
Updates per Epoch:
10000 / 100 = 100 updates

Learning Rate
Controls how much weights change during training.
Small Learning Rate:
•	Slow training 
•	Better accuracy 
Large Learning Rate:
•	Fast training 
•	May overshoot optimum solution 
Common Values:
0.1
0.01
0.001

Loss Function
Measures prediction error.
Examples:
Binary Crossentropy
Binary Classification
Categorical Crossentropy
Multi-class Classification
Mean Squared Error
Regression Problems
Goal:
Minimize loss.

Updates model weights.
Popular Optimizers:
1.	SGD 
2.	Adam 
3.	RMSProp 
4.	Adagrad 
Adam is most commonly used because it combines speed and stability.

Gradient Descent
Optimization algorithm used to reduce loss.
Steps:
1.	Predict output 
2.	Calculate loss 
3.	Compute gradients 
4.	Update weights 
5.	Repeat 
The neural network gradually learns by reducing errors during training.
Importance of Deep Learning
Deep learning can automatically learn complex features from raw data without manual feature engineering.
Applications include:
•	Computer Vision 
•	Natural Language Processing 
•	Healthcare 
•	Finance 
