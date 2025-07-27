# Final Report: Food Delivery Time Prediction

## Key Findings

- **Data Preprocessing:**  
    - Missing values were imputed (mean for numeric, most frequent for categorical).
    - Categorical features were label-encoded.
    - Continuous features were normalized.
    - Haversine distance was calculated for geospatial features.
    - Target variable (`Delayed`) was created based on median delivery time.

- **Feature Importance:**  
    - Features such as distance, delivery person experience, ratings, and tip amount were included.
    - Geospatial distance was engineered and proved useful.

## Model Evaluations

| Model         | Accuracy | Precision | Recall | F1-score |
|---------------|----------|-----------|--------|----------|
| Naive Bayes   | 1.00     | 1.00      | 1.00   | 1.00     |
| KNN           | 0.48     | 0.50      | 0.43   | 0.46     |
| Decision Tree | 0.98     | 1.00      | 0.95   | 0.98     |

- **Naive Bayes:**  
    - Achieved perfect accuracy, precision, recall, and F1-score on the test set.
    - Simple and fast, but may not capture complex relationships.

- **KNN:**  
    - Performed poorly (accuracy: 0.48).
    - Sensitive to feature scaling and parameter selection.

- **Decision Tree:**  
    - High accuracy (0.98) and perfect precision.
    - Highly interpretable and suitable for extracting decision logic.

## Actionable Recommendations

- **Recommended Model:**  
    - **Naive Bayes** is recommended for deployment due to its perfect accuracy and simplicity.
    - **Decision Tree** is a strong alternative, especially if model interpretability is a priority.

- **Operational Insights:**  
    - Focus on reducing delivery times for orders with high geospatial distance and low delivery person experience.
    - Encourage tipping and maintain high restaurant/customer ratings to improve delivery outcomes.

- **Next Steps:**  
    - Validate models on larger and more diverse datasets.
    - Explore ensemble methods for further performance gains.
    - Integrate model predictions into operational dashboards for real-time decision support.

---