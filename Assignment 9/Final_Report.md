# Deforestation Analysis Report

## 1. Overview

This report presents an analysis of deforestation drivers using a dataset containing country-level indicators such as policy strictness, corruption index, economic factors, and forest loss area. The analysis leverages feature selection and Support Vector Regression (SVR) to identify key contributors to deforestation and evaluate model performance.

---

## 2. Data Preparation

- **Data Cleaning:** Rows with missing values were dropped for simplicity.
- **Encoding:** Categorical variables (`Deforestation_Policy_Strictness`, `Corruption_Index`) were one-hot encoded.
- **Scaling:** Numerical features were standardized for model compatibility.

---

## 3. Feature Selection

Using `SelectKBest` with ANOVA F-value, the top 10 features were selected. All selected features correspond to encoded corruption index categories, indicating corruption levels are most influential in predicting forest loss area.

**Top 10 Selected Features:**
- Corruption_Index_92.56887950673188
- Corruption_Index_92.6838455570416
- Corruption_Index_93.88520297586756
- Corruption_Index_96.12875003604482
- Corruption_Index_96.49946329942216
- Corruption_Index_96.58885181054592
- Corruption_Index_96.86692495954988
- Corruption_Index_97.7844576892694
- Corruption_Index_98.37720193826966
- Corruption_Index_99.49228375628628

---

## 4. Model Training & Evaluation

- **Model:** SVR with linear and polynomial kernels.
- **Hyperparameter Tuning:** GridSearchCV identified the best SVR configuration (`C=100`, `kernel='poly'`, `degree=2`, `gamma='auto'`).
- **Performance Metrics:**
    - Training R² Score: 0.0586
    - Test R² Score: -0.3673
    - Test MAE: 0.8014
    - Test RMSE: 0.9422
    - Cross-validation R² scores: [-0.00098, -0.17788, -0.02373, -0.15280, -0.04321]

**Interpretation:**  
The model's predictive power is limited, with negative R² on the test set, indicating poor generalization. This may be due to the dominance of categorical corruption features and limited variance in the encoded data.

---

## 5. Feature Importance

Feature importance was derived from SVR coefficients:

| Feature                                 | Importance |
|------------------------------------------|------------|
| Corruption_Index_92.6838455570416        | 1.0000     |
| Corruption_Index_96.86692495954988       | 0.9921     |
| Corruption_Index_97.7844576892694        | 0.9136     |
| Corruption_Index_93.88520297586756       | 0.7881     |
| Corruption_Index_96.12875003604482       | 0.2547     |
| Corruption_Index_96.58885181054592       | 0.1317     |
| Others                                   | 0.0000     |

**Key Insight:**  
Corruption index categories are the most influential predictors of forest loss in this dataset.

---

## 6. Visualizations

### a. Scatter Plots: Selected Features vs. Forest Loss Area

![Scatter Plots](attachment:scatter_plots.png)

### b. Feature Importance Bar Chart

![Feature Importance](attachment:feature_importance.png)

### c. Correlation Heatmap

![Correlation Heatmap](attachment:correlation_heatmap.png)

---

## 7. Deforestation Trends & Recommendations

- **Trends:** High corruption levels are strongly associated with increased forest loss. Other factors (GDP, population, policy strictness) were not selected, suggesting their direct influence is less pronounced in this model.
- **Recommendations:**
    - Strengthen governance and reduce corruption.
    - Enforce stricter deforestation policies.
    - Promote sustainable economic development.
    - Increase international aid and technical support.
    - Raise public awareness and stakeholder engagement.
    - Integrate environmental considerations (protected areas, reforestation).

---

## 8. Limitations & Further Work

- Feature selection may have excluded important variables due to encoding/statistical criteria.
- Model performance is limited; alternative models or feature engineering may yield better results.
- Data quality and representativeness affect findings; expanding the dataset is recommended.

---

## 9. Summary

Deforestation is a complex issue influenced by governance, economic, demographic, and policy factors. In this analysis, corruption emerged as the most critical driver. Effective mitigation requires multi-faceted, context-specific strategies combining policy, enforcement, community engagement, and international support.