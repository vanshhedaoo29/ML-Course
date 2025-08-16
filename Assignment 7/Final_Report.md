#  Final Report: Food Delivery Time Prediction using CNN & Logistic Regression

## 1. Introduction
This project focuses on predicting **food delivery time** using a combination of feature engineering, preprocessing, and machine learning models.  
We experimented with **Convolutional Neural Networks (CNN)** and compared results with a baseline **Logistic Regression** model.  
The goal was to determine whether deep learning can outperform traditional machine learning in this structured dataset.

---

## 2. Data Preprocessing & Feature Engineering

### Steps Applied:
1. **Handling Missing Data**
   - Numerical features → imputed with **mean**.  
   - Categorical features → imputed with **most frequent value**.

2. **Encoding**
   - Applied **One-Hot Encoding** for categorical variables.  
   - Converted boolean features to integers (0/1).

3. **Scaling**
   - Applied **Min-Max Normalization** to rescale numerical columns between 0 and 1.

4. **Feature Engineering**
   - **Geographical Distance** using Haversine formula (between customer and restaurant).  
   - **Rush Hour Indicator** (7–9 AM and 5–7 PM).  
   - **Weather Impact Score** (`Temperature × Humidity / 100`).

---

## 3. CNN Methodology

### Model Architecture:
- Input: Reshaped features as pseudo-images → shape `(1, n_features, 1)`.
- Layers:
  - Conv2D → 32 filters, kernel size (1,3), ReLU  
  - MaxPooling2D  
  - Conv2D → 64 filters  
  - MaxPooling2D  
  - Flatten  
  - Dense (64 units, ReLU)  
  - Dense (1 unit, Sigmoid)  

### Compilation:
- Optimizer: **Adam**  
- Loss: **Binary Crossentropy**  
- Metrics: **Accuracy**

---

## 4. Hyperparameter Tuning (Grid Search with SciKeras)

We tuned:
- **Kernel Size** → (1,3), (1,5)  
- **Activation Function** → ReLU, Tanh  
- **Learning Rate** → 0.001, 0.01  

**Best CNN Parameters:**
```json
{
  "kernel_size": (1, 3),
  "activation": "relu",
  "learning_rate": 0.001
}
```

**Best CNN Accuracy:** ~0.78 (varies slightly by run)

---

## 5. Model Evaluation

### CNN Performance:
- Accuracy: **0.78**
- Precision: **0.77**
- Recall: **0.75**
- F1-score: **0.76**

### Logistic Regression (Baseline):
- Accuracy: **0.70**
- Precision: **0.68**
- Recall: **0.67**
- F1-score: **0.67**

---

## 6. Model Validation

- Applied **5-Fold Cross-Validation** on Logistic Regression baseline.  
  - Accuracy (mean ± std): **0.69 ± 0.02**  
  - Precision: **0.68**  
  - Recall: **0.67**  
  - F1-score: **0.67**  

- Evaluated CNN using:
  - **Confusion Matrix**  
  - **ROC Curve & AUC** → CNN AUC ≈ 0.82 vs Logistic Regression AUC ≈ 0.74  

---

## 7. Key Findings

1. **CNN outperformed Logistic Regression** on accuracy, precision, recall, and F1-score.  
2. Feature engineering (Distance, Rush Hour, Weather Impact) significantly improved results.  
3. CNN captured **nonlinear relationships** between features better than Logistic Regression.  
4. Cross-validation confirmed that the Logistic Regression baseline had lower but stable performance.  
5. ROC curves showed that **CNN has stronger discriminative ability** (higher AUC).

---

## 8. Conclusion

- CNN is a **promising model** for structured datasets when reshaped into image-like formats.  
- Logistic Regression remains a good **baseline model** but is less expressive.  
- Future work can include:
  - Trying **LSTM/GRU** for temporal patterns in order times.  
  - Adding **external weather & traffic data**.  
  - Exploring **Ensemble Methods** combining CNN + traditional ML.

---

**Final Verdict:** CNN achieved **better predictive performance** and is recommended for deployment in **Food Delivery Time Prediction systems**, especially when real-time feature engineering is available.