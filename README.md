# 💧 Water Quality Analysis – Potability Prediction

## 📌 Overview
This project focuses on analyzing **water quality** and predicting whether water is **potable (safe for drinking)** or not using various chemical features.  

Safe drinking water is essential for human health. By building an ML pipeline, this project helps in **identifying unsafe water sources** before human consumption.

---

## 📂 Dataset
- File: `water_potability.csv`  
- Rows: **3,276**  
- Columns: **10**  
- Target Variable: **Potability**  
  - `0` → Non-potable water  
  - `1` → Potable water  

**Features (Chemicals):**
- pH  
- Hardness  
- Solids  
- Chloramines  
- Sulfate  
- Conductivity  
- Organic_carbon  
- Trihalomethanes  
- Turbidity  

---

## 🔧 Data Preprocessing
1. **Handling Missing Values**  
   - Mean imputation for `pH`, `Sulfate`, and `Trihalomethanes`  
2. **Removing Duplicates**  
3. **Standardization** using `StandardScaler`  
4. **Class Balancing** using **SMOTE (Synthetic Minority Oversampling Technique)**  

---

## 📊 Exploratory Data Analysis (EDA)
Key insights generated with **Plotly interactive visualizations**:
- 🔹 **Top features influencing potability:** pH, Sulfate, Hardness, Chloramines, Solids  
- 🔹 **Correlation analysis:** No extreme multicollinearity detected  
- 🔹 **Outlier detection:** Extreme values identified for some chemicals  
- 🔹 **pH vs Potability:** Potable water is more common in the normal pH range  
- 🔹 **Feature distributions:** Potable vs Non-potable water shows chemical differences  

---

## 🏗️ Feature Selection
Based on EDA + Feature Importance (Random Forest):
- ✅ Selected top 5 features:  
  **pH, Sulfate, Hardness, Chloramines, Solids**

---

## 🤖 Machine Learning Model
**Chosen Model:** Random Forest Classifier  

**Pipeline:**
1. Feature Scaling (StandardScaler)  
2. Oversampling with SMOTE  
3. Random Forest with Hyperparameter Tuning  
4. Evaluation using **20-Fold Cross Validation**

---

## ⚙️ Hyperparameter Tuning
Optimized using Randomized Search:
- `n_estimators = 100–300`  
- `max_depth`  
- `min_samples_split`  
- `max_features`  
- Class weights for imbalance handling  

---

## 📈 Model Evaluation
**Final Model Performance (Random Forest + SMOTE + Hyperparameter Tuning + 20-Fold CV):**

| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.7447  |
| Precision    | 0.7482  |
| Recall       | 0.7377  |
| F1-Score     | 0.7429  |
| ROC-AUC      | 0.8233  |

✅ **ROC-AUC > 0.82** → strong model performance  
✅ Balanced precision & recall  

---

## 🔬 Feature Importance
Random Forest importance ranking:
1. pH  
2. Sulfate  
3. Hardness  
4. Chloramines  
5. Solids  

Helps stakeholders monitor **key chemicals** for safe water supply.  

---

## 📊 K-Fold Cross Validation Results
| K-Fold | Accuracy | Precision | Recall  | F1-Score | ROC-AUC |
|--------|----------|-----------|---------|----------|---------|
| 5      | 0.7297   | 0.7304    | 0.7282  | 0.7293   | 0.8079  |
| 10     | 0.7370   | 0.7402    | 0.7302  | 0.7352   | 0.8153  |
| 15     | 0.7382   | 0.7421    | 0.7302  | 0.7361   | 0.8207  |
| 20     | 0.7447   | 0.7482    | 0.7377  | 0.7429   | 0.8233  |

📌 **Best performance with 20-Fold CV**  

---

## 📌 Final Insights
- **Top chemicals to monitor:** pH, Sulfate, Hardness, Chloramines, Solids  
- Regular chemical monitoring ensures safe drinking water  
- Model assists in **early detection of unsafe water**  
- Interactive Plotly visualizations make insights accessible  

---

## ✅ Conclusion
- The **best performing model** is:  
  **Random Forest + Top 5 Features + SMOTE + Hyperparameter Tuning + 20-Fold CV**  
- Achieved **Accuracy ~74.5%** and **ROC-AUC 0.8233**  
- Provides reliable and interpretable predictions for **water potability analysis**  

---

## 📌 Tech Stack
- Python 🐍  
- Pandas, NumPy, Scikit-learn  
- Imbalanced-learn (SMOTE)  
- Random Forest, Cross Validation  
- Plotly (EDA & Visualizations)  

---

## 👨‍💻 Author
- **Rahul Verma**  
📧 [rahulverma69124@gmail.com]  
🌐 [https://www.linkedin.com/in/rahulverma169/]  

---

