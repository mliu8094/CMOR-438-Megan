# The Perceptron

This directory contains an implementation of the perceptron algorithm, a supervised learning method used for binary classification. In this project, the algorithm is applied to a dataset combining public transit usage and socioeconomic indicators to classify whether a city is transit-reliant (label 1) or car-reliant (label 0).

## Overview

The perceptron is a type of linear classifier that learns a weight vector to separate data points into two classes using a linear decision boundary. It computes a weighted sum of the input features and passes it through a sign activation function. It iteratively updates the weights based on errors in prediction:

A visual from Dr. Davila's CMOR 438/INDE 577 repository that outlines the percptron model:

<img width="661" alt="ThePerceptronImage (1)" src="https://github.com/user-attachments/assets/afc3b927-f739-42cb-ae42-1be1472925dc" />

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

- `perceptron.py`: Core implementation using Scikit-learn
- `transit_dataset.csv`: Dataset with urban transit and socioeconomic features
- `visualization.ipynb`: Jupyter notebook with data exploration and model training
- `README.md`: This documentation
