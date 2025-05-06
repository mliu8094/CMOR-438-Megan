# Neural Network Model

This directory contains an implementation of a basic neural network built using Keras (TensorFlow backend). The model is applied to socioeconomic and transportation-related indicators to classify outcomes such as road injury risk, economic development levels, or infrastructure quality. Here, I will be using this algorithm to predict road mortalities based on various metrics.

## Overview

A neural network is a supervised learning algorithm inspired by the structure of the human brain. It consists of layers of interconnected nodes (neurons), which can learn complex patterns by adjusting weights and biases through a process called backpropagation. Each neuron applies a mathematical operation to its inputs and passes the result through an activation function.

This implementation uses a fully connected feedforward neural network with ReLU activations in the hidden layers.

### Algorithm

Let:
- $x \in \mathbb{R}^9$: Input vector  
- $W^{[l]},\ b^{[l]}$: Weights and biases for layer $l$  
- $z^{[l]} = W^{[l]} a^{[l-1]} + b^{[l]}$: Linear combination  
- $a^{[l]}$: Activation of layer $l$  
- $\hat{y}$: Predicted output  

1. Layer 1 (64 neurons, ReLU):
   $$
   z^{[1]} = W^{[1]}x + b^{[1]}
   $$

   $$
   a^{[1]} = \text{ReLU}(z^{[1]}) = \max(0, z^{[1]})
   $$

2. Layer 2 (32 neurons, ReLU):

   \[
   z^{[2]} = W^{[2]}a^{[1]} + b^{[2]}
   \]
   \[
   a^{[2]} = \text{ReLU}(z^{[2]}) = \max(0, z^{[2]})
   \]

3. Output Layer (1 neuron, Sigmoid):

   \[
   z^{[3]} = W^{[3]}a^{[2]} + b^{[3]}
   \]
   \[
   \hat{y} = \sigma(z^{[3]}) = \frac{1}{1 + e^{-z^{[3]}}}
   \]

### ReLU

ReLU (Rectified Linear Unit) is the most commonly used activation function in neural networks. It introduces non-linearity and is defined as:

\[
\text{ReLU}(x) = 
\begin{cases}
x & \text{if } x > 0 \\
0 & \text{if } x \leq 0
\end{cases}
\]

ReLU helps prevent the vanishing gradient problem and allows models to converge faster by only activating positive signals.

### Evaluation

The performance of the neural network model is evaluated using **Mean Squared Error (MSE)**, a standard loss function for regression tasks. MSE measures the average squared difference between the predicted values and the actual target values.

$$
\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

Where:

- y_i is the actual (true) value  
- \hat{y}_i is the predicted value  
- n is the number of data points  

A lower MSE indicates better model performance, since predictions are closer to the actual values.

## Files Included

- `NeuralNetwork.ipynb`: Neural network model implementation  
- `README.md`: This documentation file
