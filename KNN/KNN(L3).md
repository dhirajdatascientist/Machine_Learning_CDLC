In the K-Nearest Neighbors (KNN) algorithm, `n_neighbors` is a parameter that specifies how many neighbors will be used to make a prediction for a new data point. 

When `n_neighbors=3`, it means that the algorithm will use the three closest data points (or "neighbors") in the feature space to make a prediction. 

Here's a bit more detail:

- **Classification:** 
    - The algorithm will identify the 3 nearest data points to the point we want to predict and will assign the most common label (or class) among those 3 neighbors to the new point.
    - For instance, if we're predicting whether a customer will buy a product (1=will buy, 0=won’t buy), and the 3 nearest neighbors have labels `[1, 0, 1]`, the algorithm will predict `1` (will buy) since two out of three neighbors have that label.

- **Regression:** 
    - The 3 nearest data points are identified and the prediction is made by averaging their values.
    - If the output values of the 3 neighbors are `[100, 120, 110]`, the algorithm will predict `(100+120+110)/3 = 110` for the new data point.
    
Choosing the right `n_neighbors` (often denoted as "K") is crucial:
- Too small a K (e.g., 1 or 2) can be noisy and sensitive to outliers.
- Too large a K may incorporate too many points that are far away, potentially degrading the model's performance.

Cross-validation is commonly used to find an optimal K value that minimizes the error on the unseen data.