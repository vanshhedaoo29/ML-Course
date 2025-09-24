# ML-Course - Tutedude

## Assignment 1: Food Delivery Time Prediction Summary

<details>
<summary>⬇️</summary>
This project analyzed 200 food delivery records using preprocessing and predictive modeling. Linear regression with distance, traffic, and order priority showed low predictive strength (R² = 0.0149, MAE = 25.37, MSE = 905.09). Logistic regression with traffic, weather, and experience performed moderately (accuracy = 0.38, precision = 0.31, recall = 0.26, F1 = 0.29, ROC AUC = 0.34), limited by class imbalance. Findings highlight distance, traffic, and staff experience as key factors. Recommendations include route optimization, peak-hour staffing, staff training, and continuous monitoring to reduce delays, improve efficiency, and enhance customer satisfaction.

</details>

## Assignment 2 : Global Pollution Analysis and Energy Recovery Summary

<details>
<summary>⬇️</summary>
This global pollution analysis shows wide variation in air, water, and soil pollution across countries, with high levels in Equatorial Guinea, Congo, and Ukraine. Energy recovery is inconsistent and often unrelated to pollution severity, while pollution strongly correlates with industrial waste and CO₂ emissions. Linear regression performed poorly in predicting energy recovery (R² = -0.025, MSE = 24792.81, MAE = 142.11), whereas logistic regression classified pollution severity effectively (accuracy = 0.950, precision = 0.956, recall = 0.950, F1 = 0.949). Recommendations include waste-to-energy investment, stricter policies, renewable adoption, circular economy practices, public awareness, and stronger monitoring.
</details>



## Assignment 3 : Naive Bayes, (KNN), Decision Tree [FDTP] Summary

<details>
<summary>⬇️</summary>
Data preprocessing involved imputing missing values, label-encoding categorical features, normalizing continuous variables, and calculating Haversine distance, with a `Delayed` target created from median delivery time. Feature importance highlighted distance, delivery person experience, ratings, tip amount, and geospatial distance. Model evaluations showed Naive Bayes achieved perfect performance (accuracy, precision, recall, F1-score = 1.00), KNN performed poorly (accuracy = 0.48, precision = 0.50, recall = 0.43, F1 = 0.46), and Decision Tree performed strongly (accuracy = 0.98, precision = 1.00, recall = 0.95, F1 = 0.98). Naive Bayes is recommended for deployment due to simplicity and perfect metrics, with Decision Tree as an interpretable alternative, alongside operational improvements targeting high-distance deliveries and low-experience personnel.
</details>

## Assignment 4 : Naive Bayes, (KNN), Decision Tree [GSA&ER] Summary

<details>
<summary>⬇️</summary>
The dataset of 200 country-year records included air, water, and soil pollution indices, industrial/plastic waste, energy consumption, CO₂ emissions, and socio-economic indicators. A composite `Total_Pollution_Index` was created and countries were categorized into Low, Medium, and High pollution severity. Model evaluations showed Decision Tree achieved the highest performance (accuracy = 0.975, precision = 0.977, recall = 0.975, F1 = 0.975), KNN performed well (accuracy = 0.900, precision = 0.903, recall = 0.900, F1 = 0.901), while MultinomialNB lagged (accuracy = 0.575, precision = 0.605, recall = 0.575, F1 = 0.575). Feature importance highlighted `Total_Pollution_Index` as key, leading to recommendations for integrated pollution management, stricter air quality regulations, cross-sector collaboration, and continuous monitoring.
</details>



## Assignment 5 : Neural Networks Clustering [FDTP] Summary

<details>
<summary>⬇️</summary>
Data preprocessing included imputing missing values, calculating Haversine distances, deriving a `Rush_Hour` feature, one-hot encoding, and standardization. K-Means (k=3) and hierarchical clustering revealed distinct clusters with varying average delivery times, highlighting that distance, ratings, weather, traffic, and order priority significantly impact delivery. Supervised models classified orders as `Fast` or `Delayed`, with Neural Network achieving F1 = 0.439 and the improved Neural Network reaching F1 = 0.489, outperforming Logistic Regression (F1 = 0.439). Recommendations include targeting slow clusters, route optimization, resource allocation during rush hours, dynamic adjustments based on conditions, and continuous monitoring using clustering and model predictions.
</details>



## Assignment 6 : Neural Networks Clustering [GSA&ER] Summary

<details>
<summary>⬇️</summary>
This study analyzed pollution and energy data across countries using preprocessing, feature engineering, clustering, and supervised learning. KMeans and Agglomerative clustering grouped countries with similar profiles, showing cluster-wise energy recovery (e.g., KMeans Cluster 0: 276.99 GWh). Neural network regression performed poorly (initial R² = -1.15, MSE = 51,961.44, MAE = 190.35; improved R² = -1.32, MSE = 56,200.59, MAE = 193.05), while linear regression outperformed it (R² = -0.11, MSE = 26,799.65, MAE = 145.19), indicating linear relationships dominate. Recommendations include investing in renewable energy, stricter waste regulations, cluster-based policy interventions, regional cooperation, and continuous monitoring to improve energy recovery.
</details>



## Assignment 7 : CNN, Apriori, Evaluation & Validation [FDTP]  Summary

<details>
<summary>⬇️</summary>
This assignment predicted food delivery time using feature engineering and machine learning, comparing CNN and Logistic Regression. Preprocessing included missing value imputation, one-hot encoding, scaling, and creating features such as Haversine distance, Rush Hour, and Weather Impact. CNN achieved superior performance with accuracy = 0.78, precision = 0.77, recall = 0.75, F1-score = 0.76, and AUC ≈ 0.82, outperforming Logistic Regression (accuracy = 0.70, precision = 0.68, recall = 0.67, F1-score = 0.67, AUC ≈ 0.74). CNN effectively captured nonlinear relationships, making it the recommended model, while Logistic Regression served as a stable baseline.
</details>



## Assignment 8 : CNN, Apriori, Evaluation & Validation [GSA&ER] Summary

<details>
<summary>⬇️</summary>
This assignment applied data preprocessing, feature engineering, and Apriori association rule mining to analyze pollution severity and energy recovery, with categorical features encoded and numerical features normalized. Frequent itemsets and rules showed moderate support (0.1–0.5), confidence, and lift (>1.0), indicating meaningful associations. High pollution regions often co-occurred with medium/high energy recovery. CNNs were discussed for delivery prediction, offering high accuracy (~0.78) but lower interpretability, whereas Apriori provided explicit, interpretable rules. Recommendations include targeted interventions in high-pollution areas, adopting efficient energy recovery technologies, policy prioritization using rule metrics, continuous monitoring, and integrating deep learning and rule-based insights for holistic environmental and logistics strategies.
</details>



## Assignment 9 : Deforestation Issue Analysis Using Support Vector Machine (SVM) Summary

<details>
<summary>⬇️</summary>
This analysis investigated deforestation drivers using country-level data, highlighting corruption as the dominant predictor. Data preprocessing included dropping missing values, one-hot encoding categorical features, and scaling numerical variables. Feature selection identified the top 10 corruption index categories, while SVR (poly kernel, C=100, degree=2) achieved limited predictive performance (Training R² = 0.0586, Test R² = -0.3673, MAE = 0.8014, RMSE = 0.9422, CV R² = [-0.00098, -0.17788, -0.02373, -0.15280, -0.04321]). High corruption levels strongly correlate with forest loss, suggesting interventions should focus on governance, stricter policies, sustainable development, international support, and public awareness.
</details>