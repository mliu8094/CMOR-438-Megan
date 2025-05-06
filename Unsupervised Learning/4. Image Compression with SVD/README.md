# Image Compression with Singular Value Decomposition (SVD)

This project demonstrates how image compression can be achieved using Singular Value Decomposition (SVD), a powerful linear algebra technique that reduces the amount of data needed to represent an image with minimal loss in quality. I will be using SVD to compress a colored image by various compression factors.

## Overview
SVD decomposes a matrix (such as an image) into three other matrices:  
$A = U \Sigma V^T$

Where:
- A: Original image matrix
- U: Left singular vectors
- $\Sigma$: Diagonal matrix of singular values (sorted by importance)
- $V^T$: Right singular vectors

By keeping only the top $k$ singular values, we can approximate the original image and significantly reduce its size.

## General Algorithm

1. Load the image as a 2D (grayscale) or 3D (RGB) matrix
2. For RGB images, split the image into three matrices: Red, Green, and Blue
3. Apply SVD to each matrix:  
    $A = U \Sigma V^T$
4. Choose a compression factor k, which determines how many singular values to retain
5. Truncate the matrices:
    - Keep the top k columns of U
    - Keep the top k singular values from $\Sigma$
    - Keep the top k rows of $V^T$
6. Reconstruct the compressed image for each color channel:  
    $A_k \approx U_k \Sigma_k V_k^T$
7. Stack the color channels back together (if RGB)

## Uses of SVD
- Approximate an image using only the top k singular values
- Higher compression factors result in lower rank approximations and more loss of detail
- This technique works well for storage optimization, transmission, or feature reduction

## Files Included

- `SVD.ipynb`: Implementation of SVD
- `README.md`: This documentation