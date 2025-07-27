# Final Report



# Food Delivery Time Prediction - Final Report

## 1. Dataset Description and Preprocessing

- **Dataset:** The dataset contains 200 food delivery records with features such as distance, weather and traffic conditions, delivery person experience, order priority, time, vehicle type, ratings, costs, and delivery time.
- **Preprocessing Steps:**
    - **Missing Values:** Numeric columns were filled with median values; categorical columns with mode.
    - **Categorical Encoding:** Columns like 'Weather_Conditions', 'Traffic_Conditions', and 'Vehicle_Type' were label-encoded.
    - **Feature Scaling:** Numeric features such as 'Distance', 'Delivery_sTime', and 'Order_Cost' were standardized.
    - **Feature Engineering:** Added 'Haversine_Distance' (geographical distance) and 'Rush_Hour' (based on order time).
    - **Outlier Handling:** Numeric columns were clipped at the 1st and 99th percentiles.

## 2. Model Evaluation and Comparisons

### Regression (Predicting Delivery Time)
- **Model:** Linear Regression
- **Features:** Distance, Traffic_Conditions, Order_Priority
- **Performance:**
    - Mean Squared Error (MSE): {mse:.2f}
    - Mean Absolute Error (MAE): {mae:.2f}
    - R-squared (R²): {r2:.4f}
- **Interpretation:** The model explains only a small portion of the variance in delivery time, indicating that additional features or more complex models may be needed.

### Classification (Predicting Fast vs. Delayed Delivery)
- **Model:** Logistic Regression
- **Features:** Traffic_Conditions, Weather_Conditions, Delivery_Person_Experience
- **Performance:**
    - Accuracy: {accuracy:.2f}
    - Precision: {precision:.2f}
    - Recall: {recall:.2f}
    - F1-score: {f1:.2f}
    - ROC AUC: {roc_auc:.2f}
- **Interpretation:** The classification model has moderate accuracy and low F1-score, suggesting class imbalance or limited predictive power from the selected features.

## 3. Actionable Insights and Recommendations

1. **Optimize Delivery Routes:**
    - Delivery time increases with distance and heavy traffic.
    - **Recommendation:** Implement route optimization tools to minimize distance and avoid congested areas.

2. **Adjust Staffing During Peak Periods:**
    - Deliveries during rush hours or high-traffic periods are more likely to be delayed.
    - **Recommendation:** Schedule more delivery personnel during peak times.

3. **Enhance Delivery Staff Training:**
    - More experienced delivery personnel tend to deliver faster and more reliably.
    - **Recommendation:** Invest in regular training and onboarding for new staff.

4. **Continuous Monitoring:**
    - Regularly review model predictions and operational data to identify new bottlenecks and improvement areas.

---

