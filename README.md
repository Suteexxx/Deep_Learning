
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Artificial Neural Network (ANN) Documentation</title>

<style>
body{
    font-family: Arial, sans-serif;
    line-height: 1.8;
    margin: 40px;
    background-color:#f5f7fa;
    color:#333;
}
.container{
    background:white;
    padding:40px;
    border-radius:10px;
    box-shadow:0 0 15px rgba(0,0,0,0.1);
}
h1,h2,h3{
    color:#1E3A8A;
}
table{
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}
table,th,td{
    border:1px solid #ddd;
}
th{
    background:#1E3A8A;
    color:white;
}
th,td{
    padding:12px;
    text-align:left;
}
code{
    background:#eee;
    padding:3px 5px;
    border-radius:5px;
}
ul li{
    margin-bottom:8px;
}
</style>
</head>

<body>

<div class="container">

<h1>🧠 Artificial Neural Network (ANN)</h1>

<h2>📌 Introduction</h2>

<p>
Artificial Neural Networks (ANNs) are machine learning models inspired by the human brain.
They consist of interconnected neurons arranged into layers that learn patterns from data
to perform prediction and classification tasks.
</p>

<h3>Applications</h3>

<ul>
<li>Image Classification</li>
<li>Speech Recognition</li>
<li>Medical Diagnosis</li>
<li>Sentiment Analysis</li>
<li>Recommendation Systems</li>
<li>Stock Prediction</li>
</ul>

<hr>

<h2>1. Architecture of ANN</h2>

<p>An ANN contains three types of layers:</p>

<h3>Input Layer</h3>
<p>Receives features from the dataset.</p>

<h3>Hidden Layer(s)</h3>
<p>Performs computations and extracts patterns.</p>

<h3>Output Layer</h3>
<p>Produces final prediction.</p>

<pre>
Input Layer → Hidden Layer(s) → Output Layer
</pre>

<hr>

<h2>2. Working of ANN</h2>

<h3>Step 1: Forward Propagation</h3>

<p>
Each neuron computes:
</p>

<pre>
z = wX + b
a = f(z)
</pre>

where:

<ul>
<li>w = weights</li>
<li>X = input</li>
<li>b = bias</li>
<li>f = activation function</li>
</ul>

<h3>Step 2: Loss Calculation</h3>

<p>
Difference between actual and predicted values is measured.
</p>

<pre>
Actual = 1
Predicted = 0.8

Error = 0.2
</pre>

<h3>Step 3: Backpropagation</h3>

<p>
Gradients are computed and propagated backward.
</p>

<h3>Step 4: Weight Update</h3>

<pre>
Wnew = Wold − η(dL/dW)
</pre>

where η = learning rate.

<hr>

<h2>3. Hyperparameters</h2>

<table>

<tr>
<th>Hyperparameter</th>
<th>Description</th>
</tr>

<tr>
<td>Learning Rate</td>
<td>Controls weight updates</td>
</tr>

<tr>
<td>Epochs</td>
<td>Number of complete training cycles</td>
</tr>

<tr>
<td>Batch Size</td>
<td>Number of samples processed together</td>
</tr>

<tr>
<td>Hidden Layers</td>
<td>Number of hidden layers</td>
</tr>

<tr>
<td>Neurons</td>
<td>Neurons per layer</td>
</tr>

<tr>
<td>Activation Function</td>
<td>Introduces non-linearity</td>
</tr>

<tr>
<td>Loss Function</td>
<td>Measures error</td>
</tr>

<tr>
<td>Optimizer</td>
<td>Updates weights</td>
</tr>

<tr>
<td>Dropout</td>
<td>Prevents overfitting</td>
</tr>

</table>

<hr>

<h2>4. Activation Functions</h2>

<h3>1. Sigmoid</h3>

<pre>
σ(x)=1/(1+e^-x)
Range: 0 to 1
</pre>

<b>Advantages</b>

<ul>
<li>Good for binary classification</li>
<li>Probability output</li>
</ul>

<b>Disadvantages</b>

<ul>
<li>Vanishing gradient problem</li>
<li>Slow convergence</li>
</ul>

<hr>

<h3>2. Tanh</h3>

<pre>
tanh(x)= (e^x-e^-x)/(e^x+e^-x)

Range: -1 to 1
</pre>

<b>Advantages</b>

<ul>
<li>Zero-centered output</li>
<li>Better than sigmoid</li>
</ul>

<b>Disadvantages</b>

<ul>
<li>Vanishing gradient problem</li>
</ul>

<hr>

<h3>3. ReLU</h3>

<pre>
f(x)=max(0,x)

Range: 0 to ∞
</pre>

<b>Advantages</b>

<ul>
<li>Fast computation</li>
<li>Reduces vanishing gradient</li>
<li>Most widely used</li>
</ul>

<b>Disadvantages</b>

<ul>
<li>Dead neuron problem</li>
</ul>

<hr>

<h3>4. Leaky ReLU</h3>

<pre>
f(x)=x , x>0
0.01x , x<0
</pre>

<b>Advantages</b>

<ul>
<li>Prevents dead neurons</li>
</ul>

<hr>

<h3>5. Softmax</h3>

<pre>
P(yi)=exp(xi)/Σexp(xj)
</pre>

Used for multiclass classification.

<hr>

<h2>5. Loss Functions</h2>

<h3>Mean Squared Error (MSE)</h3>

<pre>
MSE=(1/n)Σ(y-ŷ)²
</pre>

Used for regression.

<h3>Mean Absolute Error (MAE)</h3>

<pre>
MAE=(1/n)Σ|y-ŷ|
</pre>

Less sensitive to outliers.

<h3>Binary Cross Entropy</h3>

<pre>
L=−[ylog(p)+(1−y)log(1−p)]
</pre>

Used for binary classification.

<h3>Categorical Cross Entropy</h3>

<pre>
L=−Σ y log(p)
</pre>

Used for multiclass classification.

<h3>Sparse Categorical Cross Entropy</h3>

<p>
Used when labels are integers instead of one-hot encoded vectors.
</p>

<hr>

<h2>6. Optimizers</h2>

<h3>Gradient Descent</h3>

<pre>
W = W − η(dL/dW)
</pre>

<h4>Working</h4>

<ol>
<li>Calculate loss.</li>
<li>Compute gradients.</li>
<li>Update weights.</li>
<li>Repeat.</li>
</ol>

<hr>

<h3>Stochastic Gradient Descent (SGD)</h3>

<p>
Updates weights after every training sample.
</p>

Advantages

<ul>
<li>Faster convergence</li>
<li>Escapes local minima</li>
</ul>

<hr>

<h3>Momentum</h3>

<pre>
V = βV + η∇L

W = W − V
</pre>

Advantages

<ul>
<li>Reduces oscillations</li>
<li>Faster convergence</li>
</ul>

<hr>

<h3>RMSProp</h3>

<pre>
S = βS + (1−β)(∇L)²

W = W − η/(√S + ε)
</pre>

Advantages

<ul>
<li>Adaptive learning rate</li>
<li>Efficient for deep networks</li>
</ul>

<hr>

<h3>Adam Optimizer</h3>

<p>
Combines Momentum and RMSProp.
</p>

<pre>
m = β1m + (1−β1)g

v = β2v + (1−β2)g²

W = W − η × m/(√v + ε)
</pre>

Typical Parameters

<ul>
<li>Learning Rate = 0.001</li>
<li>β1 = 0.9</li>
<li>β2 = 0.999</li>
<li>ε = 10^-8</li>
</ul>

Advantages

<ul>
<li>Fast convergence</li>
<li>Adaptive learning rates</li>
<li>Works well on large datasets</li>
</ul>

<hr>

<h2>7. Advantages of ANN</h2>

<ul>
<li>Can learn complex relationships.</li>
<li>High accuracy.</li>
<li>Automatic feature extraction.</li>
<li>Supports classification and regression.</li>
<li>Handles noisy data.</li>
<li>Applicable to image, text and speech processing.</li>
</ul>

<hr>

<h2>8. Disadvantages of ANN</h2>

<ul>
<li>Requires large datasets.</li>
<li>Computationally expensive.</li>
<li>Training can be slow.</li>
<li>Hyperparameter tuning is difficult.</li>
<li>May suffer from overfitting.</li>
<li>Acts as a black-box model.</li>
</ul>

<hr>

<h2>9. Applications</h2>

<h3>Computer Vision</h3>

<ul>
<li>Image Classification</li>
<li>Face Recognition</li>
<li>Object Detection</li>
</ul>

<h3>Natural Language Processing</h3>

<ul>
<li>Chatbots</li>
<li>Sentiment Analysis</li>
<li>Machine Translation</li>
</ul>

<h3>Healthcare</h3>

<ul>
<li>Disease Detection</li>
<li>Medical Imaging</li>
</ul>

<h3>Finance</h3>

<ul>
<li>Fraud Detection</li>
<li>Stock Prediction</li>
</ul>

<hr>

<h2>Conclusion</h2>

<p>
Artificial Neural Networks are powerful machine learning models capable of learning complex patterns from data.
Their performance depends heavily on the choice of activation functions, loss functions, optimizers, and hyperparameters.
Among optimizers, Adam is the most widely used due to its fast convergence and adaptive learning capability.
</p>

</div>

</body>
</html>
```

