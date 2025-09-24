# Final Report: Deforestation Issue Analysis Using Support Vector Machine (SVM)

## Summary

This analysis investigated deforestation drivers using country-level data, highlighting corruption as the dominant predictor. Data preprocessing included dropping missing values, one-hot encoding categorical features, and scaling numerical variables. Feature selection identified the top 10 corruption index categories, while SVR (poly kernel, C=100, degree=2) achieved limited predictive performance (Training R² = 0.0586, Test R² = -0.3673, MAE = 0.8014, RMSE = 0.9422, CV R² = [-0.00098, -0.17788, -0.02373, -0.15280, -0.04321]). High corruption levels strongly correlate with forest loss, suggesting interventions should focus on governance, stricter policies, sustainable development, international support, and public awareness.


---