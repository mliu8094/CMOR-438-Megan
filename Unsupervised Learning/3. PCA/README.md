# Principal Component Analysis (PCA)

This directory contains an implementation of Principal Component Analysis (PCA), a widely-used unsupervised technique for dimensionality reduction and exploratory data analysis. PCA is especially useful for visualizing high-dimensional data and improving the performance of learning algorithms by removing noise and collinearity.

## Overview

PCA transforms the original correlated features into a set of linearly uncorrelated components called principal components, ordered by the amount of variance they capture from the data. It achieves this by computing the eigenvectors of the data's covariance matrix.

This project uses PCA to reduce transit and socioeconomic datasets with many features to 2D or 3D for clustering and visualization purposes, and to assess the underlying structure of the data. Then, I will assess the effect of PCA by applying DBSCAN before and after.

A visual outlining the centering of reduced dimension data in 2D:

![0_CgQFt5J1KWsl2ei1](https://github.com/user-attachments/assets/7d50fcf9-a138-4ed4-aede-778d7f442c9b)

### Algorithm

1. Standardize the data: Center the features by subtracting the mean and scale to unit variance
2. Compute the covariance matrix of the standardized data
3. Calculate the eigenvalues and eigenvectors of the covariance matrix
4. Sort eigenvectors by decreasing eigenvalues to find the directions of maximum variance.
5. Select the top k eigenvectors to form a new feature subspace.
6. Project the data onto this subspace to obtain the reduced dataset.

Let the data matrix be:
- $X \in \mathbb{R}^{n \times d}$:  
  $n$ samples with $d$ features

1. Standardization: Center data by subtracting the mean from each feature
- $\bar{X} = X - \mu$, where $\mu$ is the mean vector of shape $(1 \times d)$

2. Covariance Matrix: Compute the covariance matrix to understand how features vary together
- $C = \frac{1}{n - 1} \bar{X}^\top \bar{X}$

3. Eigen Decomposition: Compute eigenvalues and eigenvectors of the covariance matrix
- Solve $C v_i = \lambda_i v_i$,  
  where $\lambda_i$ are eigenvalues and $v_i$ are eigenvectors

4. Select Top $k$ Principal Components: Sort eigenvectors by descending eigenvalues and select the top $k$
- Form matrix $V_k = [v_1, v_2, \dots, v_k] \in \mathbb{R}^{d \times k}$

5. Project Data: Transform the original data into the reduced subspace
- $Z = \bar{X} \cdot V_k$,  
  where $Z \in \mathbb{R}^{n \times k}$ is the lower-dimensional representation

### Evaluation Metrics

- 2D or 3D Scatter Plots: Show clusters or trends in the reduced-dimensional space
- Assess predictions using other aforementioned algorithmns

## Files Included

- `PCA.ipynb`: Implementation of PCA
- `README.md`: This documentation
