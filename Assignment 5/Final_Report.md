# Final Report: Food Delivery Time Prediction

## 1. Methodology

### Data Preprocessing
- **Missing Values:** Numerical columns were imputed with the mean, and categorical columns with the most frequent value.
- **Feature Engineering:** 
    - Calculated missing/zero distances using the Haversine formula.
    - Derived a `Rush_Hour` feature from `Order_Time`.
- **Encoding & Scaling:** Categorical variables were one-hot encoded. Numerical features were standardized.

### Clustering Analysis
- **K-Means Clustering:** 
    - Used the elbow method to select the optimal number of clusters (`k=3`).
    - Clustered data based on relevant features, excluding target and identifiers.
    - Visualized clusters using PCA (2D).
- **Hierarchical Clustering:** 
    - Performed using selected features (traffic, weather, ratings, distance).
    - Compared cluster assignments with K-Means.

### Supervised Modeling
- **Neural Network:** 
    - Built a feedforward neural network to classify orders as `Fast` or `Delayed` (threshold: median delivery time).
    - Improved the model with more layers, `tanh` activation, and lower learning rate.
- **Logistic Regression:** 
    - Used as a baseline for comparison.

## 2. Model Evaluations

| Model                  | F1-score | Accuracy |
|------------------------|----------|----------|
| Neural Network         | 0.439    | -        |
| Improved Neural Network| 0.489    | -        |
| Logistic Regression    | 0.439    | -        |

- **Clustering:** Cluster-wise delivery time summaries revealed distinct groups with different average delivery times.
- **Cluster Comparison:** KMeans and Hierarchical clustering showed some overlap but also differences, indicating complex feature interactions.

## 3. Key Findings

- **Feature Importance:** Distance, ratings, weather, traffic, and order priority significantly impact delivery time.
- **Cluster Insights:** Certain clusters consistently have higher average delivery times. For example, clusters `[0, 2]` are slower.
- **Rush Hour Impact:** Delays are more frequent during rush hours (morning/evening).
- **Model Performance:** The improved neural network outperformed logistic regression, suggesting non-linear relationships are important.

## 4. Actionable Recommendations

1. **Target Slow Clusters:** Focus on clusters with higher average delivery times for process improvements.
2. **Route Optimization:** For high-distance orders in slow clusters, optimize routes or batch deliveries.
3. **Resource Allocation:** 
     - Increase delivery personnel during rush hours and adverse weather/traffic conditions.
     - Use real-time predictions to flag at-risk orders and prioritize them.
4. **Dynamic Strategies:** 
     - Monitor weather and traffic to adjust delivery strategies dynamically.
     - Provide incentives for delivery staff during peak and challenging periods.
5. **Continuous Monitoring:** Use clustering and model predictions to continuously identify and address bottlenecks.

---
