![[Pasted image 20240102202306.png]]

## Introduction

Hierarchical Clustering is an unsupervised machine learning algorithm that organizes data points into a hierarchy of clusters. This method creates a tree-like structure (dendrogram) to represent relationships between clusters at different levels of granularity. Two main approaches to hierarchical clustering are agglomerative (bottom-up) and divisive (top-down).

## Key Concepts

### 1. **Agglomerative and Divisive:**
   - Agglomerative hierarchical clustering starts with individual data points as separate clusters and merges them into larger clusters. Divisive hierarchical clustering begins with all data points in a single cluster and recursively divides them into smaller clusters.

### 2. **Distance Metric:**
   - The choice of a distance metric determines how the similarity or dissimilarity between clusters or data points is measured. Common metrics include Euclidean distance and cosine similarity.

### 3. **Linkage Criteria:**
   - Linkage criteria define how the distance between clusters is calculated during the merging process. Common linkage methods include:
     - **Single Linkage:** Minimum distance between any two points in the two clusters.
     - **Complete Linkage:** Maximum distance between any two points in the two clusters.
     - **Average Linkage:** Average distance between all pairs of points in the two clusters.

### 4. **Dendrogram:**
   - A dendrogram is a tree-like diagram that illustrates the hierarchical structure of clusters. It helps visualize the relationships and the order of merging or splitting.

## Hierarchical Clustering Algorithm

### Agglomerative Hierarchical Clustering:

1. **Start:**
   - Treat each data point as a single cluster.

2. **Calculate Distance:**
   - Compute the pairwise distance between all clusters.

3. **Merge Closest Clusters:**
   - Merge the two closest clusters based on the chosen linkage criteria.

4. **Update Distance Matrix:**
   - Recalculate distances between the new cluster and all remaining clusters.

5. **Repeat:**
   - Repeat steps 3 and 4 until all data points belong to a single cluster.

### Divisive Hierarchical Clustering:

1. **Start:**
   - Consider all data points as part of a single cluster.

2. **Calculate Distance:**
   - Compute the pairwise distance between all data points.

3. **Identify Split:**
   - Identify the split that maximizes the inter-cluster distance.

4. **Update Distance Matrix:**
   - Recalculate distances between the newly formed clusters and all remaining data points.

5. **Repeat:**
   - Repeat steps 3 and 4 until each data point is in a separate cluster.

![[Pasted image 20240102202321.png]]


## Advantages

1. **Hierarchy Representation:**
   - Provides a clear hierarchy of clusters, enabling users to understand relationships at different levels of granularity.

2. **No Preset Number of Clusters:**
   - Hierarchical clustering does not require specifying the number of clusters beforehand.

3. **Flexibility:**
   - Allows users to cut the dendrogram at any level to obtain the desired number of clusters.

## Challenges and Considerations

1. **Computational Complexity:**
   - Hierarchical clustering can be computationally intensive, especially for large datasets.

2. **Sensitivity to Distance Metric:**
   - The choice of distance metric can impact the resulting clusters.

3. **Difficulty in Visualizing Large Dendrograms:**
   - Visualizing large dendrograms can be challenging and may require interactive tools.

## Applications

1. **Biology:**
   - Clustering genes based on expression patterns or organisms based on genetic similarities.

2. **Marketing:**
   - Grouping customers based on purchasing behavior at different levels of detail.

3. **Image Analysis:**
   - Classifying images based on visual features at various levels of abstraction.

4. **Text Mining:**
   - Clustering documents or words based on semantic similarities.
