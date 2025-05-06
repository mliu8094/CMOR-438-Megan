# K-Means Clustering

This directory contains an implementation of the K-Means Clustering algorithm, an unsupervised learning technique used to split dataset into distinct groups based on feature similarity. I will be categorizing of some of a country's socioeconomic metrics, specifically lifespan and unemployment rate.

## Overview

K-Means clustering seeks to divide n data points into k clusters in which each point belongs to the cluster with the nearest mean (centroid). It minimizes the within-cluster sum of squares, often referred to as inertia. The algorithm works best when clusters are spherical and well-separated, and it's widely used to define categories based on data.

A visual outlining how k-means clustering creates categories based on data:

![0_VaT0CgPcagwFX1Az](https://github.com/user-attachments/assets/477bf772-97fe-480a-89e9-edf6f4718ce3)

### Algorithm

1. Choose the number of clusters k
2. Initialize centroids randomly or using a strategy like k-means++
3. Repeat until convergence:
    - Assign each data point to the nearest centroid based on Euclidean distance
    - Recalculate the centroids as the mean of all points assigned to that cluster
4. Stop when assignments no longer change or the centroids stabilize

### Evaluation Metrics of k

- Elbow Method
    - Plot inertia vs. k
    - This can tell us an optimal balance between complexity and fit
    - When inertia stops changing significantly, we know there is no longer that large of an effect of increasing k

- Silhouette Score
    - Measures how similar an object is to its own cluster versus others
    - Values range from -1 to 1 and higher is better

## Files Included

- `KMeansCLustering.ipynb`: Implementation of k means clustering
- `README.md`: This documentation
