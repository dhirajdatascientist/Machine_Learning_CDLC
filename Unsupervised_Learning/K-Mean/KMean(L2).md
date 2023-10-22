What is KMeans?

1. **What**: KMeans groups similar data together into "clusters."
2. **Why**: To find patterns or categories in data without being told them.
3. **How**: It picks center points and gathers data close to them.
4. **Use**: Helps in organizing things like customers, colors, or items.
5. **Without It**: Data remains mixed up, and patterns might be missed.

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


**Explanation**

1. `import matplotlib.pyplot as plt`: Import plotting library to visualize data.
2. `from sklearn.cluster import KMeans`: Import KMeans for data clustering.
3. `import numpy as np`: Import numpy for numerical operations.
4. `dataset = {...}`: Define a sample dataset of fruits with their weights and lengths.
5. `data = np.array(list(zip(dataset["weight"], dataset["length"])))`: Convert the dataset to a format suitable for clustering.
6. `kmeans = KMeans(n_clusters=3)`: Initialize KMeans clustering for 3 types of fruits.
7. `kmeans.fit(data)`: Train the KMeans model using the data.
8. `labels = kmeans.predict(data)`: Predict which cluster each fruit belongs to.
9. `centroids = kmeans.cluster_centers_`: Get the center point of each cluster.
10. `plt.scatter(data[:, 0], data[:, 1], c=labels, cmap='rainbow', marker='o', s=100)`: Plot the fruits on a scatter plot, colored by their cluster.
11. `plt.scatter(centroids[:, 0], centroids[:, 1], c='black', marker='x', s=150)`: Plot the center of each cluster.
12. `plt.xlabel("Weight (g)")`: Label the x-axis as "Weight".
13. `plt.ylabel("Length (cm)")`: Label the y-axis as "Length".
14. `plt.title("Fruit Clustering")`: Set the title for the plot.
15. `plt.show()`: Display the plot.


**Expanding point no.10**

10. `plt.scatter(data[:, 0], data[:, 1], c=labels, cmap='rainbow', marker='o', s=100)`:

- `plt.scatter(...)`: This function plots individual points on a 2D plane.
- `data[:, 0]`: This represents all the x-coordinates of our data points. It takes all rows (`:`) of the `data` array and only the first column (index `0`), which corresponds to the "weight" of the fruits.
- `data[:, 1]`: This represents all the y-coordinates of our data points. It takes all rows (`:`) of the `data` array and only the second column (index `1`), which corresponds to the "length" of the fruits.
- `c=labels`: The color of each data point is determined by the `labels` assigned from KMeans clustering. Each unique label will have a distinct color.
- `cmap='rainbow'`: This specifies the colormap used to assign colors based on `labels`. The 'rainbow' colormap provides a range of colors to distinguish between the different clusters.
- `marker='o'`: This sets the shape of each data point to a circle.
- `s=100`: This sets the size of each data point to 100 units, making them larger and more visible on the plot. 
