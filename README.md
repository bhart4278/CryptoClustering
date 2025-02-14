# CryptoClustering
Python and unsupervised machine learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Overview
This project applies clustering techniques to group cryptocurrencies based on their market performance. The goal is to use K-Means clustering and Principal Component Analysis (PCA) to optimize and visualize the classification of cryptocurrencies.

## Technologies Used
- Python
- Pandas
- scikit-learn
- hvPlot

## Data Preprocessing
1. **Load Data**: Import `crypto_market_data.csv` into a Pandas DataFrame.
2. **Exploratory Data Analysis**: Generate summary statistics and visualize the data.
3. **Normalize Data**: Use `StandardScaler()` from scikit-learn to standardize feature values.
4. **Prepare Data**: Create a new DataFrame with scaled values, indexed by `coin_id`.

## K-Means Clustering
### Finding Optimal k (Elbow Method)
- Iterate k values from 1 to 11 and compute inertia.
- Plot an elbow curve to identify the optimal k.
- Determine the best k value and document observations.

### Clustering with K-Means
- Initialize K-Means with the optimal k.
- Fit the model to the scaled data.
- Predict clusters and add them to the DataFrame.
- Visualize clusters using a scatter plot (`hvPlot`).

## Dimensionality Reduction with PCA
- Reduce features to three principal components.
- Compute explained variance to assess information retention.
- Create a new DataFrame with PCA-transformed data.

## K-Means on PCA Data
- Repeat the elbow method to determine the best k for PCA-transformed data.
- Compare with original k-means results.
- Cluster using K-Means and visualize the results.

## Key Questions Answered
- What is the best value for k in both cases?
- How does PCA affect clustering accuracy?
- What are the insights gained from clustering cryptocurrencies?

## Results
- Visualizations for both standard and PCA-optimized clusters.
- Comparison of clustering effectiveness before and after dimensionality reduction.

## Conclusion
This project demonstrates the power of K-Means clustering in cryptocurrency classification and highlights how PCA can improve clustering efficiency by reducing dimensionality while preserving essential information. The following elbow and clusters charts compares the PCA optimized results vs the non-optimized results:
![Screenshot 2025-02-14 at 1 02 27 PM](https://github.com/user-attachments/assets/d8d1bbf0-ba1a-4d7d-88ba-22a589a33f42)

![Screenshot 2025-02-14 at 1 02 51 PM](https://github.com/user-attachments/assets/bd3fb610-2dda-42b5-b4be-dc82a3347f03)
