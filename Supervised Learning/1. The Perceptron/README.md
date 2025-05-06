# The Perceptron

This directory contains an implementation of the perceptron algorithm, a supervised learning method used for binary classification. In this project, the algorithm is applied to a dataset combining public transit usage and socioeconomic indicators to classify whether a city is transit-reliant (label 1) or car-reliant (label 0).

## Overview

The perceptron is a type of linear classifier that learns a weight vector to separate data points into two classes using a linear decision boundary. It computes a weighted sum of the input features and passes it through a sign activation function. It iteratively updates the weights based on errors in prediction:

A visual from Medium that outlines the difference between the linear and logistic regression models:



### Algorithm

1. Initialize weights and bias to zero (or small random values).
2. For each training sample:
   - Compute the predicted label (weighted sums)
   - Compare it to the actual label  
   - If the prediction is incorrect, update the weights:  
       `w ← w - η * (predicted - actual) * x`  
       `b ← b - η * (predicted - actual)`
3. Repeat for a number of epochs or until convergence.

## Files Included

- `Perceptron.ipynb`: Perceptron implementation
- `README.md`: This documentation
