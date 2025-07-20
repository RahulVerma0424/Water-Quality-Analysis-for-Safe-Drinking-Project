# Water Quality Analysis for Safe Drinking – Machine Learning Project

## Problem Statement

The quality of drinking water is crucial for public health. Contaminated water can cause serious diseases like cholera, typhoid, and diarrhea. This project aims to **analyze water samples and predict whether the water is safe for drinking**, using machine learning models trained on physicochemical properties.

---

## Dataset Overview

The dataset consists of various features related to water quality parameters:

| Feature | Description |
|--------|-------------|
| pH | Acidity/alkalinity of water |
| Hardness | Presence of calcium and magnesium |
| Solids | Total dissolved solids |
| Chloramines | Disinfectant used in water |
| Sulfate | Naturally occurring substance |
| Conductivity | Water’s ability to pass electrical flow |
| Organic_carbon | Organic pollutants present |
| Trihalomethanes | Disinfection byproducts |
| Turbidity | Cloudiness due to particles |
| Potability | **Target Variable** (1 = Safe, 0 = Unsafe) |

---

## Exploratory Data Analysis (EDA)

- Checked for missing values and replaced them using median imputation.
- Analyzed distribution and correlation between features.
- Visualizations included:
  - Countplots for Potability
  - Boxplots to detect outliers
  - Heatmap to see feature correlation
  - Histograms for individual distributions

 Observations:
- pH, Sulfate, and Organic Carbon significantly affect potability.
- Several features show mild to moderate correlation.

---


##  Model Building

Tested multiple classification algorithms to predict potability:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- XGBoost Classifier

---

## Model Evaluation

### Evaluation Metrics Used:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

 **Best Performing Model: XGBoost Classifier**
- Accuracy: ~78%
- ROC-AUC Score: ~0.81
- Balanced Precision & Recall

---

## Conclusion

### What did we learn?
- Water features like **pH, Organic Carbon, and Trihalomethanes** play an important role in classifying potability.
- ML models, especially ensemble methods like Random Forest and XGBoost, perform well for binary classification of water safety.

### Business-Level Insights:
- Governments and health organizations can deploy such models to **automatically flag unsafe water samples**, especially in rural or under-monitored areas.

---

## Future Enhancements

- Use larger, more diverse datasets with regional labeling.
- Include external factors like **temperature**, **pipe age**, or **water source**.
- Deploy as a mobile or web app with live predictions.
- Add a **dashboard** using Streamlit or Flask for visual inspection.

---

## Tools & Libraries Used

| Tool/Library | Use |
|--------------|-----|
| Python | Core language |
| Pandas, NumPy | Data handling |
| Matplotlib, Seaborn, Plotly | Visualization |
| Scikit-learn | ML models & metrics |
| XGBoost | Advanced classification |
| Jupyter Notebook | Dev environment |

---

## How to Run

```bash
1. Clone the repository
2. Run the notebook: `Water Quality Analysis for Safe Drinking Project.ipynb`
3. Follow through the cells to see step-by-step model building and predictions
