
Firstly, install `scikit-learn` and `numpy` if you haven't done it yet:
```bash
pip install scikit-learn numpy
```

Now, let's create a small Python script:

```python
import numpy as np
from sklearn.neighbors import KNeighborsClassifier

# Sample Data: [Age, Income]
X = np.array([
    [25, 50000],
    [35, 36000],
    [45, 45000],
    [35, 25000],
    [50, 60000]
])

# Labels: Will buy(1), Won't buy(0)
y = np.array([1, 0, 1, 0, 1])

# Create KNN classifier
knn = KNeighborsClassifier(n_neighbors=3)

# Fit the classifier to the data
knn.fit(X, y)

# Predict the label for a new customer: [Age, Income]
new_customer = np.array([40, 48000]).reshape(1, -1)
prediction = knn.predict(new_customer)

print("Prediction for new customer (Will buy=1, Won't buy=0):", prediction[0])
```

**Explanation:**
- `X`: This is our feature matrix, each inner array represents a data point with 2 features: age and income.
- `y`: This is our target vector, which contains the labels (1 if they will buy, 0 if not) for each data point.
- We initialize a KNN classifier object with `KNeighborsClassifier(n_neighbors=3)`, meaning we're using K=3.
- `knn.fit(X, y)`: Here, we're fitting our model to the data. Despite the fact KNN is a lazy learner (no actual training phase), `fit` method organizes the data in a way that the prediction phase could be optimized.
- We then predict the label for a new data point (`new_customer`) using `knn.predict(new_customer)`.
- Lastly, we print out the prediction.

**Note:** Remember that KNN is sensitive to scales between features. In practice, you might want to scale your features (for instance, using `MinMaxScaler` or `StandardScaler` from `scikit-learn`) to ensure that the distance metric is not unduly influenced by one of the features. This simple example skips that step for the sake of clarity.
