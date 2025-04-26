**KNN Theory**

## K-Nearest Neighbors (KNN)

**Definition:**  
KNN is a non-parametric, instance-based learning algorithm that classifies (or regresses) a new data point based on the labels (or values) of its *k* nearest neighbors in the feature space.

**How it works:**
1. Choose a number of neighbors, **k**.  
2. Compute the distance (e.g. Euclidean, Manhattan) from the query point to all points in the training set.  
3. Select the **k** points with the smallest distances.  
4. **Classification:** Assign the label that is most common among the neighbors.  
   **Regression:** Predict the average (or weighted average) of their values.

| Aspect                   | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| **Type**                 | Lazy learning, non-parametric                                           |
| **Distance Metric**      | Euclidean, Manhattan, Minkowski, Cosine, etc.                           |
| **Decision Rule**        | Majority vote (classification) or mean/weighted mean (regression)       |
| **Key Hyperparameters**  | `n_neighbors` (k), `weights` (uniform or distance-based), `p` (Minkowski exponent) |
| **Training Time**        | O(1) (stores data only)                                                 |
| **Prediction Time**      | O(n) per query (distance to all training points)                        |
| **Advantages**           | - Simple to understand & implement  
- No explicit training phase  
- Naturally handles multi-class |
| **Limitations**          | - Slow on large datasets  
- Sensitive to feature scaling and irrelevant features  
- Memory-intensive (stores all training data) |
| **When to use**          | - Small to medium datasets  
- Problems where simplicity and interpretability matter |
