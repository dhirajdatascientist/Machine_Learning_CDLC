Let's assume you have the following dataset:

```python
dataset = {
    "fruit": ["apple", "apple", "banana", "banana", "grape", "grape"],
    "weight": [150, 155, 120, 125, 5, 6],
    "length": [8, 8.5, 20, 19.5, 2, 2.5]
}
```

Given this dataset, we want to cluster the fruits based on their weight and length:

```python
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import numpy as np

# Dictionary Dataset
dataset = {
    "fruit": ["apple", "apple", "banana", "banana", "grape", "grape"],
    "weight": [150, 155, 120, 125, 5, 6],
    "length": [8, 8.5, 20, 19.5, 2, 2.5]
}

# Convert dictionary values to a numpy array for clustering
data = np.array(list(zip(dataset["weight"], dataset["length"])))

# Using KMeans to cluster the data into 3 clusters
kmeans = KMeans(n_clusters=3)
kmeans.fit(data)
labels = kmeans.predict(data)
centroids = kmeans.cluster_centers_

# Plotting the data and the centroids
plt.scatter(data[:, 0], data[:, 1], c=labels, cmap='rainbow', marker='o', s=100)
plt.scatter(centroids[:, 0], centroids[:, 1], c='black', marker='x', s=150)
plt.xlabel("Weight (g)")
plt.ylabel("Length (cm)")
plt.title("Fruit Clustering")
plt.show()
```

