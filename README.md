🧠 Artificial Neural Network (ANN)
📌 Introduction

An Artificial Neural Network (ANN) is a machine learning model inspired by the biological neural network of the human brain. It consists of interconnected nodes (neurons) organized into layers that learn patterns from data and make predictions.

ANNs are widely used in:

Image Classification
Speech Recognition
Sentiment Analysis
Recommendation Systems
Medical Diagnosis
Financial Forecasting
📚 Table of Contents
Architecture of ANN
Working of ANN
Hyperparameters
Activation Functions
Loss Functions
Optimizers
Advantages
Disadvantages
Applications
1. Architecture of ANN

An ANN generally consists of three types of layers:

Input Layer

Receives features from the dataset.

Hidden Layer(s)

Performs computations and extracts patterns.

Output Layer

Produces the final prediction.

Input Layer → Hidden Layer(s) → Output Layer

Example:

784 Inputs → 128 Neurons → 64 Neurons → 10 Outputs
2. Working of ANN
Step 1: Forward Propagation

Input data passes through neurons.

For each neuron:

z=wX+b

where:

w = weights
X = input
b = bias

Output becomes

a=f(z)

where f is the activation function.

Step 2: Loss Calculation

Difference between actual and predicted values is measured using a loss function.

Example:

Actual = 1
Predicted = 0.8

Error = 0.2
Step 3: Backpropagation

Error is propagated backward and gradients are calculated.

Step 4: Weight Update

Optimizer updates weights:

W
new
	​

=W
old
	​

−η
∂W
∂L
	​


where

η = learning rate
L = Loss
3. Hyperparameters

Hyperparameters are parameters set before training.

Hyperparameter	Description
Learning Rate	Controls step size during optimization
Epochs	Number of complete passes through dataset
Batch Size	Number of samples processed at once
Hidden Layers	Number of hidden layers
Neurons	Number of neurons per layer
Activation Function	Introduces non-linearity
Optimizer	Updates weights
Loss Function	Measures prediction error
Dropout Rate	Prevents overfitting
Weight Initialization	Initial values of weights
Common Hyperparameter Values
Learning Rate
0.1
0.01
0.001 (Most common)
0.0001
Batch Size
16
32
64
128
256
Epochs
10
50
100
200
4. Activation Functions

Activation functions introduce non-linearity and help neural networks learn complex patterns.

(1) Sigmoid

Formula:

σ(x)=
1+e
−x
1
	​


Range:

0 to 1

Advantages:

Good for binary classification.
Produces probability values.

Disadvantages:

Vanishing gradient problem.
Slow convergence.
(2) Tanh

Formula:

tanh(x)=
e
x
+e
−x
e
x
−e
−x
	​


Range:

-1 to 1

Advantages:

Zero-centered outputs.
Better than sigmoid.

Disadvantages:

Vanishing gradient problem.
(3) ReLU (Rectified Linear Unit)

Formula:

f(x)=max(0,x)

Range:

0 to ∞

Advantages:

Fast computation.
Most widely used.
Reduces vanishing gradient.

Disadvantages:

Dead neuron problem.
(4) Leaky ReLU

Formula:

f(x)={
x,
0.01x,
	​

x>0
x<0
	​


Advantages:

Solves dead neuron problem.
(5) Softmax

Formula:

P(y
i
	​

)=
∑e
x
j
	​

e
x
i
	​

	​


Used for:

Multi-class classification

Example:

Cat = 0.8
Dog = 0.15
Horse = 0.05
5. Loss Functions

Loss functions measure prediction error.

(1) Mean Squared Error (MSE)

Formula:

MSE=
n
1
	​

∑(y−
y
^
	​

)
2

Used for:

Regression problems

Advantages:

Simple
Differentiable
(2) Mean Absolute Error (MAE)

Formula:

MAE=
n
1
	​

∑∣y−
y
^
	​

∣

Used for:

Regression

Less sensitive to outliers.

(3) Binary Cross Entropy

Formula:

L=−[ylog(p)+(1−y)log(1−p)]

Used for:

Binary Classification

Examples:

Spam detection
Disease prediction
(4) Categorical Cross Entropy

Formula:

L=−∑ylog(p)

Used for:

Multi-class Classification

Examples:

MNIST digit recognition
Image classification
(5) Sparse Categorical Cross Entropy

Used when labels are integers instead of one-hot encoded vectors.

Example:

Labels:
0,1,2,3...
6. Optimizers

Optimizers update weights to minimize loss.

(1) Gradient Descent

Update Rule:

W=W−η
∂W
∂L
	​

Working
Compute loss.
Calculate gradients.
Update weights.
Repeat.
Disadvantages
Slow convergence.
Can get stuck in local minima.
(2) Stochastic Gradient Descent (SGD)

Updates weights after every sample.

Advantages
Faster.
Escapes local minima.
Disadvantages
Noisy updates.
(3) Mini-Batch Gradient Descent

Updates weights using a batch of samples.

Typical batch sizes:

32
64
128

Balances speed and stability.

(4) Momentum

Adds previous gradients to current updates.

Update equations:

V = βV + η∇L

W = W − V

Advantages:

Faster convergence.
Reduces oscillations.
(5) RMSProp

Adjusts learning rate adaptively.

Update:

S = βS + (1−β)(∇L)^2

W = W − η/(√S+ε)

Advantages:

Efficient for deep networks.
Handles non-stationary data.
(6) Adam (Adaptive Moment Estimation)

Most widely used optimizer.

Combines:

Momentum
RMSProp

Equations:

m = β₁m + (1−β₁)g

v = β₂v + (1−β₂)g²

W = W − η × m/(√v + ε)

Typical values:

Learning rate = 0.001
β1 = 0.9
β2 = 0.999
ε = 10^-8
Advantages

✔ Fast convergence

✔ Adaptive learning rates

✔ Suitable for large datasets

✔ Most commonly used optimizer

7. Advantages of ANN

✅ Learns complex nonlinear relationships.

✅ High accuracy for large datasets.

✅ Handles noisy data.

✅ Automatic feature extraction.

✅ Supports classification and regression.

✅ Can model highly complex problems.

✅ Applicable to image, text, and speech data.

8. Disadvantages of ANN

❌ Requires large datasets.

❌ Computationally expensive.

❌ Training can be slow.

❌ Hyperparameter tuning is difficult.

❌ Overfitting may occur.

❌ Acts as a black-box model.

❌ Requires powerful hardware for deep networks.

9. Applications of ANN
Computer Vision
Image Classification
Object Detection
Face Recognition
Natural Language Processing
Chatbots
Sentiment Analysis
Machine Translation
Healthcare
Disease Detection
Medical Imaging
Finance
Fraud Detection
Stock Prediction
Recommendation Systems
Netflix
Amazon
YouTube
Autonomous Vehicles
Lane Detection
Traffic Sign Recognition
Conclusion

Artificial Neural Networks are powerful machine learning models capable of learning complex relationships from data. Their performance depends heavily on the choice of activation functions, loss functions, optimizers, and hyperparameters. Optimizers like Adam and activation functions like ReLU have become standard choices due to their efficiency and effectiveness in deep learning applications.

