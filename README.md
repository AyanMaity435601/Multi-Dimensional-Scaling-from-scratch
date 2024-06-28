# Multi-Dimensional Scaling (MDS) for Visualizing MNIST Handwritten Digits

## Overview
This project implements Multi-Dimensional Scaling (MDS) to visualize the MNIST handwritten digit dataset. MNIST consists of 28x28 pixel grayscale images of handwritten digits (0-9). Each image is represented as a 784-dimensional feature vector.

## Objective
The goal is to reduce the dimensionality of the MNIST dataset from 784 dimensions to 2 dimensions using MDS. This reduction allows us to visualize the high-dimensional data in a 2D space while preserving the pairwise distances between samples as much as possible.

## Implementation Details
- **Data Loading:**
  - The MNIST dataset is loaded from gzip files (`train-images-idx3-ubyte.gz` and `train-labels-idx1-ubyte.gz` for training images and labels respectively).
  - Training images and labels are read using custom functions (`read_images` and `read_labels`).

- **MDS Implementation:**
  - Euclidean distances between all pairs of samples are computed to create a distance matrix.
  - Centering matrix and B matrix are computed as per MDS formulation.
  - Eigenvalue decomposition of B matrix is performed to obtain eigenvectors and eigenvalues.
  - The top eigenvalues and corresponding eigenvectors are selected to project the data into a lower-dimensional space (2D).

- **Visualization:**
  - The reduced 2D dataset is visualized using matplotlib.
  - Each digit (0-9) is plotted with a distinct color to observe clustering and patterns in the data.

## Result
- The MDS algorithm successfully reduces the 784-dimensional MNIST dataset to 2 dimensions.
- Visualization of the 2D projection shows clusters corresponding to different digits, demonstrating the effectiveness of MDS in preserving the data structure.


---

This README provides an overview of the project, details on the implementation of MDS, its application to the MNIST dataset, and the visualization of the results. It aims to clarify the purpose, method, and outcome of using MDS for dimensionality reduction and visualization of high-dimensional data.
