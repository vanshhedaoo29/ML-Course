# Final Report: Global Pollution Analysis

## Key Findings

- **Data Overview:** The dataset includes pollution indices (air, water, soil), industrial and plastic waste, energy consumption, CO2 emissions, and socio-economic indicators for 200 country-year records.
- **Feature Engineering:** A composite `Total_Pollution_Index` was created by summing scaled air, water, and soil pollution indices. All pollution indices were standardized for fair comparison.
- **Pollution Severity:** Countries/years were categorized into `Low`, `Medium`, and `High` pollution severity based on quantiles of the total index.

## Model Evaluations

| Model           | Accuracy | Precision | Recall | F1-score |
|-----------------|----------|-----------|--------|----------|
| MultinomialNB   | 0.575    | 0.605     | 0.575  | 0.575    |
| KNN             | 0.900    | 0.903     | 0.900  | 0.901    |
| Decision Tree   | 0.975    | 0.977     | 0.975  | 0.975    |

- **Decision Tree** outperformed other models with 97.5% accuracy and F1-score, indicating strong predictive power for pollution severity classification.
- **KNN** also performed well (90% accuracy), while **MultinomialNB** lagged behind, likely due to its assumptions not fitting the data distribution.
- **Confusion Matrices** show that the Decision Tree model made almost perfect predictions across all classes.

## Feature Importance

- The Decision Tree model identified `Total_Pollution_Index` as the most influential feature for predicting pollution severity, with all importance weight assigned to it.

## Actionable Recommendations

Based on model insights and feature importance:

- **Integrated Pollution Management:** Since `Total_Pollution_Index` is the dominant predictor, policies should target multiple pollution sources simultaneously for maximum impact.
- **Air Quality Regulations:** Implement stricter air quality standards, promote clean energy, and incentivize reduction of industrial emissions.
- **Cross-Sector Collaboration:** Encourage cooperation between environmental, industrial, and energy sectors to address pollution holistically.
- **Continuous Monitoring:** Invest in data collection and monitoring to track pollution trends and policy effectiveness.

---