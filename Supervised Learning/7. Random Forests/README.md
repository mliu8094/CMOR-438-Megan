# Random Forests

This directory contains an implementation of the Random Forest algorithm, an ensemble learning method used for both classification and regression tasks. In this project, the model is applied to predict the same road mortaliy rate in the neural network model. I will be analyzing various ensemble methods, starting with random forests to assess the performance of each.

## Overview

A Random Forest is an ensemble of decision trees. Each tree is trained on a random subset of the data and a random subset of features, helping to reduce overfitting and improve generalization. The final prediction is made by averaging (for regression) or majority voting (for classification) across all the trees.

Random Forests combine the simplicity of decision trees with the power of ensemble learning to improve prediction accuracy and robustness.

### Characteristics about the Random Forest Model

- Reduces variance from single decision trees
- Handles large feature spaces well
- Can estimate feature importance
- Works for both classification and regression

## Algorithm

1. Bootstrap Sampling: For each tree, sample the training data with replacement (bootstrapping)
2. Random Feature Selection: At each node split, choose a random subset of features to consider
3. Grow Decision Tree: Fully grow the tree on the sampled data until a stopping condition is met
4. Repeat Steps 1–3 for many iterations of trees
5. Predictions:
   - Regression: Average the predictions from all trees
   - Classification: Use majority vote

## Evaluation Metrics

For regression, the following metrics are commonly used:
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- ${R}^{2}$ Score

For classification, evaluation includes:
- Accuracy
- Confusion Matrix

## Files Included

- `RandomForests.ipynb`: Implementation of random forests
- `README.md`: This documentation