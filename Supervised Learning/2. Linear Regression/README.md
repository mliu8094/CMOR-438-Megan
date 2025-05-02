# Linear Regression

This directory contains an implementation of the linear regression algorithm, a fundamental supervised learning technique used to model the relationship between a dependent variable and one or more independent variables. In this project, linear regression is applied to a dataset that includes transportation data such as air transit passenger quantity and population in a country's largest city to predict greenhouse gas (primarily CO2) emissions.

## Overview

Linear regression aims to fit a straight line (or hyperplane in higher dimensions) that best describes the relationship between the input features and the target variable. It minimizes the error between predicted and actual values using a method called least squares. The resulting model can be used to make continuous predictions, such as estimating emissions based on city characteristics.

A visual from Dr. Davila's CMOR 438/INDE 577 repository that outlines the percptron model:

<img width="661" alt="ThePerceptronImage (1)" src="https://github.com/user-attachments/assets/afc3b927-f739-42cb-ae42-1be1472925dc" />

### Algorithm

1. Initialize weights and bias to zero (or small random values).
2. For each training sample:
   - Use the formula ŷ = mx + b to compute predictions.
   - Optimize weights (m in this case) and bias (b in this case) by minimizing the Mean Squared Error (MSE) between predicted and actual values
3. Evaluate performance using metrics:
   - RMSE (Root Mean Squared Error): measures average prediction error
   - R^2 score: indicates the proportion of variance explained by the model

## Files Included

- `LinearRegression.ipynb`: Linear regression model implementation
- `README.md`: This documentation
