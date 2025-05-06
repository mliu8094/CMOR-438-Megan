# K-Nearest Neighbors

This directory contains an implementation of the K-Nearest Neighbors (KNN) algorithm, a simple, instance-based supervised learning method used for classification. In this project, the KNN algorithm is applied to a dataset of socioeconomic and public transit indicators to classify what population of a country has completed secondary school based on metrics like GDP, internet access, population, etc.

## Overview

K-Nearest Neighbors is a distance-based algorithm that stores all available cases and classifies new cases based on a similarity measure (Euclidean distance in this case). It does not explicitly learn a model but makes predictions based on the majority class of the k closest training points.

Here is an illustrative diagram of the KNN concept from Dr. Davila's CMOR 438/INDE 577 repository:


### Algorithm

1. Choose the number of neighbors k
2. For a new data point:
   - Compute the distance between this point and all other points in the training dataset
   - Sort the distances and identify the k closest neighbors
   - Take a vote for classification from the labels of these neighbors
3. Assign the class based on majority voting
4. Repeat for all test data points

### Mathematical Description

- $x \in \mathbb{R}^n$: new input vector  
- $D = \{(x_1, y_1), (x_2, y_2), ..., (x_m, y_m)\}$: training dataset  
- Compute Euclidean distance:  
  $d(x, x_i) = \sqrt{ \sum_{j=1}^{n} (x_j - x_{ij})^2 }$
- Select the k smallest distances and assign the class by majority vote

### Evaluation

The performance of the KNN regression is evaluated using standard metrics such as:
- Error and ${R}^{2}$: Mean squared error, mean absolute error, etc.
- Plot actual vs. predicted to see how closely values align

## Files Included

- `KNN_Classifier.ipynb`: KNN model implementation
- `README.md`: This documentation file


