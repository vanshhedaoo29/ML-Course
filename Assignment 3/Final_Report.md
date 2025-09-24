# Final Report: Food Delivery Time Prediction

## Summary

Data preprocessing involved imputing missing values, label-encoding categorical features, normalizing continuous variables, and calculating Haversine distance, with a `Delayed` target created from median delivery time. Feature importance highlighted distance, delivery person experience, ratings, tip amount, and geospatial distance. Model evaluations showed Naive Bayes achieved perfect performance (accuracy, precision, recall, F1-score = 1.00), KNN performed poorly (accuracy = 0.48, precision = 0.50, recall = 0.43, F1 = 0.46), and Decision Tree performed strongly (accuracy = 0.98, precision = 1.00, recall = 0.95, F1 = 0.98). Naive Bayes is recommended for deployment due to simplicity and perfect metrics, with Decision Tree as an interpretable alternative, alongside operational improvements targeting high-distance deliveries and low-experience personnel.

---


