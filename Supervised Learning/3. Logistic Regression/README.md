# Logistic Regression

This directory contains an implementation of the logistic regression algorithm, a supervised learning method used for binary classification. In this project, the algorithm is applied to a dataset combining public transit usage and socioeconomic indicators to predict whether a city is predict the quality of transit infrastructure based on GDP per capita. Mean values of various good quality transit infrstructure (1). For our purposes, if the average value of transit quality between the different modes are transit are above a certain threshold, then the transit quality is good (1) and otherwise it is poot (0).

## Overview

Logistic regression is a linear model for classification that estimates the probability that a given input point belongs to a particular class. Instead of using a step function like the perceptron, logistic regression uses the sigmoid function to map predicted values to probabilities between 0 and 1. The model is trained by minimizing the log-loss using gradient descent.

A visual from Dr. Davila's CMOR 438/INDE 577 repository that outlines the logistic regression model:

<img width="661" alt="LogisticRegressionImage" src="https://upload.wikimedia.org/wikipedia/commons/6/6d/Exam_pass_logistic_regression.png" />

### Algorithm

1. Initialize parameters:
   - Set the weights vector to zeros, one for each feature.
   - Set the bias term to zero.

2. Iterate over a number of epochs (controlled by `n_iters`):
   - Compute the linear combination of inputs and weights:  
     `z = X · weights + bias`
   - Apply the sigmoid function to convert the output to probabilities:  
     `ŷ = 1 / (1 + exp(-z))`
   - Compute the gradients of the loss with respect to weights and bias:
     - `dw = (1/n) * Xᵀ · (ŷ - y)`
     - `db = (1/n) * sum(ŷ - y)`
   - Update parameters using gradient descent:
     - `weights ← weights - learning_rate * dw`
     - `bias ← bias - learning_rate * db`

3. Prediction:
   - To predict probabilities: apply sigmoid to the linear output.
   - To classify: label as 1 if probability > 0.5, else 0.

## Files Included

- `LogisticRegression.ipynb`: Logistic regression implementation
- `README.md`: This documentation
