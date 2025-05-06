# K-Means Clustering

This directory contains an implementation of DBSCAN (Density-Based Spatial Clustering of Applications with Noise), an unsupervised clustering algorithm particularly effective for identifying clusters of arbitrary shape and handling noise in the dataset. In this directory, DBSCAN is used to find groupings using lifespan and unemployment rate that may not conform to well-separated, spherical clusters.

## Overview

DBSCAN is a density-based clustering algorithm that groups together points that are closely packed together (i.e., with many nearby neighbors), and marks points that lie alone in low-density regions as outliers or noise. Unlike k-Means, DBSCAN does not require the number of clusters to be specified beforehand and is capable of discovering clusters of various shapes and sizes.

A visual outlining how k-means clustering creates categories based on data:

### Algorithm

1. Define two parameters:
    eps: Maximum distance between two points for them to be considered as in the same neighborhood
    min_samples: Minimum number of points required to form a dense region (core point)

2. For each point in the dataset:
    If the number of points within eps is greater than or equal to min_samples, the point is a core point
    If it is within eps of a core point, it is a border point
    Otherwise, it is labeled as noise.

3. Clusters are formed from connected core points and their reachable neighbors.

### Evaluation Metrics of k

- Elbow Method
    - Plot inertia vs. k
    - This can tell us an optimal balance between complexity and fit
    - When inertia stops changing significantly, we know there is no longer that large of an effect of increasing k

- Number of clusters: A good DBSCAN run should produce a meaningful number of clusters
- Percentage of noise points: Indicates how many points were excluded as outliers

## Files Included

- `DBSCAN.ipynb`: Implementation of DBSCAN
- `README.md`: This documentation
