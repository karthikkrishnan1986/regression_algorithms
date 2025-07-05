```markdown
# Customer Churn Prediction — End-to-End Machine Learning Project

This project predicts whether a telecom customer is likely to churn using logistic regression. It's a complete workflow that includes data cleaning, preprocessing, feature engineering, class imbalance handling, model building, evaluation, and interpretation.

---

## Problem Statement

Customer churn is when a customer stops doing business with a company. The goal of this project is to build a machine learning model that can predict churn so that proactive retention strategies can be applied.

---

## Dataset

- **Source:** Telco Customer Churn dataset
- **Records:** 7,043
- **Target column:** `Churn` (Yes / No)
- **Features:** Demographics, services subscribed, contract details, billing, etc.

---

## Key Steps

### 1. Data Cleaning
- Converted `TotalCharges` from object to numeric.
- Handled 11 missing values (customers with 0 tenure → set `TotalCharges = 0`).

### 2. Feature Engineering
- One-hot encoded categorical variables with `pd.get_dummies()`.
- Mapped `Churn`: `Yes → 1`, `No → 0`
- Created `TotalCharges_numeric` column
- Feature scaling using `StandardScaler`

### 3. Class Imbalance Handling
- Used `class_weight='balanced'` in logistic regression
- Helped the model focus on the minority class (churners)

### 4. Model Building
- Trained logistic regression on preprocessed data
- Evaluated with confusion matrix and classification report

---

## Results

| Metric (Churn - Class 1) | Value |
|--------------------------|--------|
| Recall                   | **78%** |
| Precision                | 50% |
| F1-Score                 | 61% |
| Accuracy                 | 74% |

> Focused on **recall** to ensure churners are correctly identified, even at the cost of some precision.

---

## Takeaways

- Logistic regression performed well with proper preprocessing
- `class_weight='balanced'` is a simple and effective technique to address class imbalance
- Scaling improved consistency, although it didn’t significantly change results
- Churn was strongly correlated with features like `Contract`, `Tenure`, and `MonthlyCharges`

---

## Future Enhancements

- Try **SMOTE** for oversampling the minority class
- Train **Random Forest** and **XGBoost**
- Use **SHAP** or **permutation importance** for explainability
- Package the model into a reusable pipeline

---

## How to Run

1. Clone the repository  
2. Install dependencies  
3. Open the notebook `churn_analysis.ipynb`  
4. Run all cells to reproduce results

---

## Connect with Me

- [LinkedIn](https://www.linkedin.com/in/karthik-krishnan-18642533/)
- ⭐ Star the repo if you find it helpful!

```
