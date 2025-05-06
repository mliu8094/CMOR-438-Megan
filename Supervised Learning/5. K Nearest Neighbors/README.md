# K-Nearest Neighbors

This directory contains an implementation of the K-Nearest Neighbors (KNN) algorithm, a simple, instance-based supervised learning method used for classification. We evaluated KNN's classification capabilities in class, so I am interested in exploring whether using KNN regression is ever predictive. As a result, in this project, the KNN algorithm is applied to a dataset of socioeconomic and public transit indicators to classify what population of a country has completed secondary school based on metrics like GDP, internet access, population, etc.

## Overview

K-Nearest Neighbors is a distance-based algorithm that stores all available cases and classifies new cases based on a similarity measure (Euclidean distance in this case). It does not explicitly learn a model but makes predictions based on the majority class of the k closest training points.

A visual outlining how KNN would be used for classification or regression:

<img width="739" alt="Screen-Shot-2017-06-17-at-9 30 39-AM-1" src="https://github.com/user-attachments/assets/38f8c047-e23f-4841-afcd-133156418bfa" />

### Algorithm

1. Choose the number of neighbors k
2. For a new data point:
   - Compute the distance between this point and all other points in the training dataset
   - Sort the distances and identify the k closest neighbors
   - Take a vote for classification from the labels of these neighbors
3. Assign the class based on majority voting for classification or compute the average of the target values (labels) of these k neighbors for regression
4. Repeat for all test data points

### Mathematical Description

- $x \in \mathbb{R}^n$: new input vector  
- $D = \{(x_1, y_1), (x_2, y_2), ..., (x_m, y_m)\}$: training dataset  
- Compute Euclidean distance:  
  $d(x, x_i) = \sqrt{ \sum_{j=1}^{n} (x_j - x_{ij})^2 }$
- Select the k smallest distances and assign the class by majority vote or mean of k neighbors

### Evaluation

The performance of the KNN regression is evaluated using standard metrics such as:
- Error and ${R}^{2}$: Mean squared error, mean absolute error, etc.
- Plot actual vs. predicted to see how closely values align

## Files Included

- `KNN_Classifier.ipynb`: KNN model implementation
- `README.md`: This documentation file


