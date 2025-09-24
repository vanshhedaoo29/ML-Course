# Final Report: Neural Networks Clustering [FDTP]

## Summary

Data preprocessing included imputing missing values, calculating Haversine distances, deriving a `Rush_Hour` feature, one-hot encoding, and standardization. K-Means (k=3) and hierarchical clustering revealed distinct clusters with varying average delivery times, highlighting that distance, ratings, weather, traffic, and order priority significantly impact delivery. Supervised models classified orders as `Fast` or `Delayed`, with Neural Network achieving F1 = 0.439 and the improved Neural Network reaching F1 = 0.489, outperforming Logistic Regression (F1 = 0.439). Recommendations include targeting slow clusters, route optimization, resource allocation during rush hours, dynamic adjustments based on conditions, and continuous monitoring using clustering and model predictions.


---
