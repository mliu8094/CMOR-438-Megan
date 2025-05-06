# Ensemble Learning: Boosting and Voting Regression

This directory explores advanced ensemble methods, Boosting and Voting Regression, which are used for improving predictive performance in both regression and classification tasks. These models combine multiple "weak" learners to produce a more accurate and robust model. I will be analyzing the same target as before, road mortality, to understand which model can provide the most predictive result.

## Overview

Ensemble methods combine the predictions from multiple models to improve accuracy, reduce variance, and handle complex datasets more effectively. While bagging methods like Random Forest reduce variance by averaging independent models, boosting focuses on reducing bias by sequentially correcting errors made by previous models.

### Included Methods

- Boosting (e.g., Gradient Boosting, AdaBoost, XGBoost)
- Voting Regression

### Characteristics

- Higher accuracy
- Can handle non-linear data well
- Works well with tabular datasets

A visual outlining XGBoost for classification from GeeksforGeeks:

![Bagging](https://github.com/user-attachments/assets/a1c0892b-0f75-46a7-bb3e-77307cde8375)

## Boosting

Boosting builds an ensemble of models in a sequential manner. Each model tries to correct the errors made by the previous one.

### Key Characteristics

- Trains models one after another
- Focuses more on difficult examples in each step
- Common variants:
  - Gradient Boosting Regressor
  - AdaBoost
  - XGBoost

### Algorithm (XGBoost)

1. Initialize predictions with a base value (e.g., mean of targets for regression)
2. For each boosting round t=1 to T:
    - Compute the gradients
    - Compute the Hessians (second derivative of loss)
    - Fit a regression tree to the gradients and Hessians
    - Choose splits that maximize the gain and add tree to ensemble
3. Final prediction is the sum of outputs from all trees:

## Voting Regression

Voting Regression combines predictions from multiple different regression models and averages them to improve performance.

### Types
- Hard Voting: Used for classification
- Soft Voting (Averaging):
  - Takes the average of predictions from multiple models such as:  
        - Linear Regression  
        - Decision Tree Regressor  
        - Random Forest  
        - K-Nearest Neighbors Regressor  

## Files Included

- `EnsembleMethods.ipynb`: Implementation of random forests
- `README.md`: This documentation
