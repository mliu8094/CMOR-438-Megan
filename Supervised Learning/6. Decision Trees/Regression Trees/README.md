# Decision Trees / Regression Trees

This directory contains an implementation of decision and regression trees, which is a supervised learning method used for classification and regression tasks. In this project, the model is used to predict whether or not a country has a high or low mortality rate from disease based on a variety of features in both a classification and regression capacity.

## Overview

Decision trees are models that split data into regions based on feature values. Each internal node represents a decision (or test) on a feature, each branch represents the outcome of the test, and each branching node represents a final output or prediction.

In regression trees, instead of predicting class labels, the model predicts a continuous value, typically by averaging the target variable in each leaf.

### Visual Example

A visual of a regression tree that splits the data based on conditions of feature values:


## Algorithm

1. Start with all data at the root
2. For each feature and possible split value:
   - Partition the data into two subsets
   - Compute the mean squared error for the split
3. Choose the split that minimizes the MSE
4. Recursively apply the splitting process to the left and right subsets
5. Stop splitting when:
   - A maximum depth is reached,
   - The number of samples is too small,
   - Or no further gain can be achieved
6. Prediction is the mean value of target variables in the corresponding branching node

## Loss Function

For regression, decision trees typically minimize the **Mean Squared Error (MSE)**:

$$
\text{MSE} = \frac{1}{N} \sum_{i=1}^N (y_i - \hat{y}_i)^2
$$

Where:
- $y_i$ is the true value,
- $\hat{y}_i$ is the predicted value,
- $N$ is the number of samples.

## Evaluation Metrics

Evaluation metrics for decision or regression trees include:
- For classification: confusion matrix between correct and incorrect predictions
- Error metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE)
- ${R}^{2}$ Score (Coefficient of Determination)

## Files Included

- `DecisionTreeRegressor.ipynb`: Main implementation of regression tree
- `README.md`: This documentation
- `dataset.csv`: Example dataset used to train and test the model