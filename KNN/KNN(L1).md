## KNN

* K-Nearest Neighbors (KNN) is a simple, yet powerful machine learning algorithm used for classification and regression. It works on the principle that objects with similar features tend to be in the same category. So, the algorithm classifies an object based on how its neighbors are classified.

**Key points about KNN:**
1. **No Training Phase:** Unlike other machine learning algorithms, KNN doesn't have a training phase. All the data is used during the testing phase.
2. **Distance Metric:** It uses a distance metric (like Euclidean, Manhattan, etc.) to find the nearest neighbors.
3. **Number of Neighbors (K):** The user must specify the number of neighbors to be considered while classifying the new data point.
4. **Classification/Regression:** For classification, a vote is held among the K-nearest neighbors, and the majority class is assigned to the test point. For regression, the average of K-nearest neighbors is computed.

**Example:**

Imagine we have a tiny dataset of people with two features: their age and their income. The task is to predict whether each person buys a specific product or not.

```plaintext
| Age  | Income ($) | Buy Product (Yes=1/No=0) |
|------|------------|--------------------------|
| 25   | 50,000     | 1                        |
| 35   | 36,000     | 0                        |
| 45   | 45,000     | 1                        |
| 35   | 25,000     | 0                        |
| 50   | 60,000     | 1                        |
```

Suppose we have a new customer, age 40, income $48,000, and we want to predict whether they will buy the product.

If K=3 (i.e., we look at the three nearest neighbors):
- We calculate the distance between our new customer and all others using a distance metric (e.g., Euclidean distance).
- Find the 3 neighbors with the smallest distances.
- For classification: Use a majority vote among the 3-nearest neighbors to predict whether the new customer will buy the product. If, for instance, 2 neighbors have "1" and 1 neighbor has "0" in "Buy Product", we predict that the new customer will buy the product.
- For regression: Compute the average output variable among the K-nearest neighbors.

**Notes:**
- **Choosing K:** A small K value (like 1 or 2) can be noisy and subject to outliers, while a large K might be computationally expensive and might include neighbors that are too far away.
- **Feature Scaling:** KNN is sensitive to different scales among features, so it's often crucial to normalize/standardize data.
- **Computational Cost:** As the dataset grows, KNN can become computationally expensive since it needs to compute the distance to every data point in the dataset.

In a nutshell, KNN leverages the similarity between instances of data to predict the output for new instances. It's simple, intuitive, and can be quite effective in certain applications.