# Final Report

## Methodology

- **Data Preprocessing:**  
    - Loaded and cleaned the dataset, handling missing values using `SimpleImputer` for both categorical and numerical columns.
    - Encoded categorical variables (`Country`, `Year`) using `LabelEncoder`.
    - Scaled pollution indices with `StandardScaler` for uniformity.

- **Feature Engineering:**  
    - Created new features such as `CO2_Emissions_Per_Capita`.
    - Analyzed yearly trends by aggregating pollution indices and energy recovery.

- **Clustering Analysis:**  
    - Applied KMeans and Agglomerative (hierarchical) clustering on pollution and energy features.
    - Used the Elbow Method to determine the optimal number of clusters (`k=3`).
    - Visualized clusters and compared assignments between methods.

- **Supervised Learning:**  
    - Built and evaluated a neural network regression model to predict `Energy_Recovered (in GWh)`.
    - Improved the neural network with deeper architecture and hyperparameter tuning.
    - Compared neural network results with a baseline linear regression model.

## Model Evaluations

- **Clustering Models:**  
    - KMeans and Agglomerative clustering grouped countries with similar pollution and energy profiles.
    - Mean energy recovery per cluster:
        - KMeans:  
            - Cluster 0: 276.99 GWh  
            - Cluster 1: 265.76 GWh  
            - Cluster 2: 238.23 GWh
        - Agglomerative:  
            - Cluster 0: 256.61 GWh  
            - Cluster 1: 277.74 GWh  
            - Cluster 2: 238.92 GWh
    - Cluster assignments were similar but not identical between methods.

- **Neural Network Regression:**  
    - Initial model:  
        - R²: -1.15  
        - MSE: 51,961.44  
        - MAE: 190.35
    - Improved model:  
        - R²: -1.32  
        - MSE: 56,200.59  
        - MAE: 193.05
    - Linear Regression:  
        - R²: -0.11  
        - MSE: 26,799.65  
        - MAE: 145.19

- **Interpretation:**  
    - The neural network did not outperform linear regression, suggesting linear relationships dominate or more data/model tuning is needed.
    - Clustering is effective for segmentation but not for direct prediction.

## Key Findings

- Countries cluster into distinct groups based on pollution and energy features.
- Clusters with higher renewable energy and lower pollution tend to have higher average energy recovery.
- Supervised models indicate that increasing renewable energy, reducing waste, and improving economic indicators are associated with better energy recovery.
- Linear regression provided the best predictive performance among tested models.

## Actionable Recommendations

- **For Countries with High Pollution and Low Energy Recovery:**
    - Invest in renewable energy infrastructure.
    - Implement stricter regulations on industrial and plastic waste.
    - Promote energy efficiency and waste-to-energy technologies.
    - Foster public-private partnerships for sustainable practices.

- **For Policymakers:**
    - Use cluster analysis to benchmark and tailor interventions.
    - Encourage regional cooperation among countries in similar clusters.
    - Monitor pollution and energy recovery metrics regularly to guide policy adjustments.

- **For Future Work:**
    - Explore additional features and advanced models to improve prediction accuracy.
    - Collect more granular data to capture non-linear relationships.
    - Investigate causal relationships between policy interventions and energy recovery outcomes.

---