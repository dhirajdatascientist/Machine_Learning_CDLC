## Test your skills

1. **Basic Understanding**:
   - What is K-means clustering?
   - Ans- Covert a data into a cluster from which is similar data.
   - here we finding the same pattern or categories. 

2. **Initialization**:
   - How is the initial value of the centroids usually determined in K-means clustering?
  ans.  - the first centroid is selected randomly from the data points.
   - 

3. **Algorithm Steps**:
   - Briefly describe the steps involved in the K-means clustering algorithm.
   Ans. - import numpy as np
   - from sklearn.cluster import KMeans
   -data=[[]]
   - df = np.array([data]
   - kmeans = KMeans(n_clusters=4)
   - kmeans.fit(data)
   - labels=kmeans.labels_
   - for i,label in enumerate(labels):
   - print(label+1)

4. **Python Implementation**:
   - Which Python library provides a direct implementation of the K-means clustering algorithm?
Ans.import numpy as np its means numpy
5. **Choosing K**:
   - How can you determine the optimal number of clusters (K) for your dataset?
   - Elbow Method.
   -  Silhouette Coefficient
   -  Gap Statistic

6. **Convergence**:
   - How does the K-means algorithm determine that it has converged?
   - Centroid Stability
   - Cluster Assignment Consistency
   - Within-Cluster Sum of Squares (WCSS) Stabilization.
   - 

7. **Distances**:
   - Which distance metric is commonly used to compute the similarity between data points and centroids in K-means?
   - Euclidean distance. 

8. **Limitations**:
   - What are some limitations of the K-means clustering algorithm?
   - Requirement for Pre-defined Cluster Count
   - Sensitivity to Initialization
   - Assumption of Spherical Cluster Shapes
   - Sensitivity to Outliers
   - Limitation to Numerical Data
   - Difficulty with High-Dimensional Data
   - Convergence to Local Minima
   - Challenges with Clusters of Varying Density
   - Unsuitability for Arbitrary Distance Measures
   -   
   - 

9. **Code Snippet**:
   - Given the following code, what will be the number of clusters formed?
     ```python
     from sklearn.cluster import KMeans
     kmeans = KMeans(n_clusters=3)
     kmeans.fit(data)
     ```
     Ans. 3 clusters.
   
10. **Visualization**:
   - How can you visualize the clusters formed by K-means on a 2D dataset in Python?
   - Ans. import matplotlib.pyplot as plt
