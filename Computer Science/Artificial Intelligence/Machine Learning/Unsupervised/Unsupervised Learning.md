![[Pasted image 20231218163053.png]]

# Unsupervised Learning

## Introduction

Unsupervised learning is a category of machine learning where the algorithm is not provided with labeled training data. Instead, the algorithm explores the inherent structure and patterns within the data without explicit guidance. Unsupervised learning is often used for tasks such as clustering, dimensionality reduction, and density estimation.

## Key Concepts

### 1. **No Labels:**
   - In unsupervised learning, the algorithm is not provided with target labels for the training data. The goal is to discover hidden patterns or structures within the data.
### 2. **Exploratory Nature:**
   - Unsupervised learning is exploratory in nature, aiming to reveal the underlying relationships and groupings within the data.
### 3. **Clustering:**
   - Clustering involves grouping similar instances together based on certain characteristics or features. It helps identify natural divisions in the data.
### 4. **Dimensionality Reduction:**
   - Dimensionality reduction techniques aim to reduce the number of features in the data while preserving its essential characteristics. This helps in visualizing and understanding high-dimensional data.
### 5. **Density Estimation:**
   - Density estimation involves estimating the probability distribution of the data, providing insights into the likelihood of different values or events occurring.

## Unsupervised Learning Techniques

### 1. **[[Clustering]]:**
   - **K-Means Clustering:**
     - Divides the dataset into 'k' clusters based on similarity, where 'k' is a user-defined parameter.
   - **Hierarchical Clustering:**
     - Organizes data into a hierarchy of clusters. Instances are successively grouped together to form a tree-like structure.
   - **DBSCAN (Density-Based Spatial Clustering of Applications with Noise):**
     - Identifies clusters based on the density of data points, allowing for the detection of irregularly shaped clusters.
### 2. **[[Dimensionality Reduction]]:**
   - **Principal Component Analysis (PCA):**
     - Reduces the dimensionality of the data by transforming it into a new set of orthogonal features (principal components) that capture the maximum variance.
   - **t-Distributed Stochastic Neighbor Embedding (t-SNE):**
     - Focuses on preserving the pairwise similarities between instances in a lower-dimensional space, often used for visualization.
### 3. **Association Rules:**
   - **Apriori Algorithm:**
     - Discovers frequent itemsets in transactional databases, helping identify patterns and associations among items.
### 4. **[[Generative Models]]:**
   - **Gaussian Mixture Models (GMM):**
     - Represents the distribution of data as a mixture of Gaussian distributions, useful for density estimation and clustering.
   - **Autoencoders:**
     - Neural network-based models designed for unsupervised learning, where the network learns to encode input data into a lower-dimensional representation and decode it back.
### 5. **[[Anomaly Detection]]:**
   - **Isolation Forest:**
     - Identifies anomalies by isolating instances through random partitioning.
   - **One-Class SVM (Support Vector Machine):**
     - Learns the distribution of normal instances and identifies deviations as anomalies.

## Applications

1. **Customer Segmentation:**
   - Clustering techniques are used to group customers based on their purchasing behavior.
2. **Anomaly Detection:**
   - Detecting unusual patterns in system logs or financial transactions.
3. **Image and Signal Processing:**
   - Dimensionality reduction techniques are applied for feature extraction in image and signal data.
4. **Market Basket Analysis:**
   - Association rules help identify patterns in consumer purchasing behavior.
5. **Biomedical Research:**
   - Unsupervised learning is used for clustering patients based on health metrics or identifying anomalous patterns in medical images.