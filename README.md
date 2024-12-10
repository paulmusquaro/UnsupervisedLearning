# UnsupervisedLearning

## Overview

This project focuses on applying unsupervised learning techniques, particularly **K-means clustering** and **Principal Component Analysis (PCA)**, to two datasets:

- **data_2d.csv**: A 2D dataset to demonstrate clustering analysis.
- **mnist.csv**: The popular MNIST dataset containing handwritten digits, where PCA is applied to reduce the dimensionality of the data before clustering.

The goal of this project is to cluster the data using the K-means algorithm, determine the optimal number of clusters using the **Elbow method**, and visualize the results. For the MNIST dataset, PCA is used to reduce the data to a 2D representation, allowing clustering to be applied in a simpler, more visualizable space.

## Project Breakdown

1. **Data Loading and Preprocessing**:
   - The datasets are loaded and cleaned. For the 2D dataset, an irrelevant column is removed before performing clustering.
   
2. **K-means Clustering**:
   - The **K-means** algorithm is applied to both datasets. The optimal number of clusters is determined using the **Elbow method**. This involves plotting the inertia (sum of squared distances to the nearest centroid) for different numbers of clusters and identifying the "elbow point," where the rate of decrease slows down.

3. **Principal Component Analysis (PCA)**:
   - PCA is applied to reduce the dimensionality of the MNIST dataset from 784 dimensions to 2 dimensions. This helps in visualizing the clustering results in a 2D space.

4. **Visualization**:
   - The clustering results are visualized with scatter plots, showing how the data points are grouped and how the centroids of the clusters are positioned.
   
5. **K-means++**:
   - The project also compares the standard K-means algorithm with **K-means++**, a method designed to initialize centroids more effectively to improve the clustering result.

## Key Findings

- For the **2D dataset**, the optimal number of clusters was found to be 4, as this division better represented the underlying data structure.
- For the **MNIST dataset**, PCA reduced the data to a 2D space, and the K-means algorithm was applied to identify 5 clusters. The **Elbow method** suggested that the optimal number of clusters lies between 3 and 5, with 5 clusters providing the best balance.

## Conda (Setup and Environment)

To make the project reproducible and ensure smooth package management, this project uses Conda as a package and environment manager. Below are the steps to set up the environment:


1. **Install Conda**:
If you haven't installed Conda yet, you can download it from the official [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) websites. Anaconda is a larger distribution with more pre-installed packages, while Miniconda is a smaller, minimal version. Choose whichever suits your needs.

2. **Create a new environment:** Open your terminal and run the following command to create a new Conda environment with Python 3.12:

    ```bash
    conda create --name new_conda_env python=3.12
    ```

3. **Activate the environment:** Once the environment is created, activate it by running:

    ```bash
    conda activate new_conda_env
    ```

4. **Install required packages (Jupyter, NumPy, MatPlotLib, Pandas and Scikit-Learn)**

    ```bash
    conda install jupyter numpy matplotlib pandas scikit-learn
    ```

5. **Run Jupyter Notebook**

    ```bash
    jupyter notebook
    ```

***

## Conclusion

This project demonstrates how unsupervised learning algorithms, specifically **K-means clustering** and **PCA**, can be used to uncover patterns in datasets. The Elbow method provided a clear way to choose the optimal number of clusters, and PCA helped in reducing the dimensionality of the MNIST dataset for easier analysis and visualization.

## Future Work

- Investigate other clustering algorithms, such as **DBSCAN** and **hierarchical clustering**, to compare their effectiveness.
- Explore more advanced dimensionality reduction techniques to improve clustering accuracy and efficiency.

