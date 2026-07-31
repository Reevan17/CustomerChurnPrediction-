# Telecom Customer Churn Prediction

A machine learning classification project that predicts whether a telecom customer is likely to churn or continue using the service based on customer demographics, services, contract details, and billing information.

The project follows a complete machine learning workflow, starting from data exploration and preprocessing to model training, evaluation, hyperparameter tuning, and final model selection.

---

## Project Objective

Customer retention is an important challenge for telecom companies. Losing existing customers can be costly compared to retaining them.

The objective of this project is to build a classification model that can identify customers who are likely to churn, allowing businesses to take proactive actions such as personalized offers, loyalty programs, and improved customer support.

---

## Project Workflow

- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Baseline Model Development
- Model Comparison
- Hyperparameter Tuning
- Final Model Selection
- Model Saving and Prediction Testing

---

## Project Structure

```
Telecom-Churn-Prediction/

│
├── data/
│   ├── raw/
│   │   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   │
│   └── processed/
│       ├── X_train.csv
│       ├── X_test.csv
│       ├── y_train.csv
│       └── y_test.csv
│
├── models/
│   └── logistic_regression_churn_model.pkl
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Data_Preprocessing.ipynb
│   ├── 03_Baseline_Model.ipynb
│   ├── 04_Model_Comparison.ipynb
│   ├── 05_Hyperparameter_Tuning.ipynb
│   └── 06_Final_Model.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Dataset

**Dataset:** Telco Customer Churn Dataset

- Rows: 7,043
- Columns: 21
- Target Variable: `Churn`

Each row represents a telecom customer. The objective is to predict whether the customer will leave the service.

---

# Exploratory Data Analysis

The following analysis was performed:

- Dataset overview
- Data type checking
- Missing value analysis
- Duplicate checking
- Target variable distribution
- Univariate analysis
- Bivariate analysis
- Business insights

### Key Insights

- Most customers do not churn.
- The dataset has a moderate class imbalance:
  - No Churn: approximately 73%
  - Churn: approximately 27%
- Month-to-month contracts have the highest churn rate.
- New customers are more likely to churn.
- Fiber optic customers show higher churn rates.
- Customers using electronic check payments have higher churn.
- Automatic payment methods are associated with lower churn.
- Senior citizens show a higher churn rate.
- Gender has little effect on churn.

---

# Data Preprocessing

The following preprocessing steps were performed:

- Converted `TotalCharges` from object to numeric format.
- Handled blank values in `TotalCharges`.
- Removed rows containing missing values.
- Dropped `customerID` as it does not contribute to prediction.
- Applied Label Encoding to binary categorical variables.
- Applied One-Hot Encoding to multi-category variables.
- Split the dataset into training and testing sets (80:20).
- Applied StandardScaler for feature scaling.
- Saved processed datasets for model training.

---

# Baseline Model

## Logistic Regression

Logistic Regression was selected as the baseline model.

Performance:

| Metric | Score |
|---|---:|
| Accuracy | 78.75% |
| Precision | 62.06% |
| Recall | 51.60% |
| F1-Score | 56.35% |
| ROC-AUC | 83.19% |

The baseline model showed good separation ability based on ROC-AUC and provided a strong starting point for comparison.

---

# Model Comparison

The following models were evaluated:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.7875 | 0.6206 | 0.5160 | **0.5635** | **0.8319** |
| Decision Tree | 0.7335 | 0.4988 | **0.5481** | 0.5223 | 0.6739 |
| Random Forest | 0.7846 | **0.6300** | 0.4599 | 0.5317 | 0.8179 |

### Observations

- Logistic Regression provided the best overall balance between precision, recall, F1-score, and ROC-AUC.
- Decision Tree achieved higher recall but suffered from overfitting.
- Random Forest achieved better precision but had lower recall compared to Logistic Regression.

---

# Hyperparameter Tuning

Random Forest was optimized using RandomizedSearchCV.

Configuration:

- 5-fold cross-validation
- F1-score used as the optimization metric
- Multiple hyperparameter combinations tested

Best parameters:

```python
{
    'n_estimators': 200,
    'max_depth': 10,
    'min_samples_split': 10,
    'min_samples_leaf': 1,
    'max_features': 'sqrt'
}
```

---

## Tuned Random Forest Performance

| Metric | Score |
|---|---:|
| Accuracy | 79.46% |
| Precision | 65.68% |
| Recall | 47.59% |
| F1-Score | 55.19% |
| ROC-AUC | 83.16% |

---

## Overfitting Analysis

Before tuning:

| Model | Training Accuracy | Testing Accuracy |
|---|---:|---:|
| Random Forest | 99.77% | 78.46% |

After tuning:

| Model | Training Accuracy | Testing Accuracy |
|---|---:|---:|
| Tuned Random Forest | 84.99% | 79.46% |

Hyperparameter tuning reduced overfitting by limiting model complexity while maintaining performance on unseen data.

---

# Final Model

After comparing all models, Logistic Regression was selected as the final model.

Reasons for selection:

- Highest F1-score
- Highest ROC-AUC score
- Better recall compared to Random Forest
- Easier interpretation for business decisions

Final model performance:

| Metric | Score |
|---|---:|
| Accuracy | 78.75% |
| Precision | 62.06% |
| Recall | 51.60% |
| F1-Score | 56.35% |
| ROC-AUC | 83.19% |

The trained model was saved using Joblib and tested by loading it back and making predictions on unseen data.

---

# Machine Learning Concepts Covered

- Binary Classification
- Exploratory Data Analysis
- Data Cleaning
- Missing Value Handling
- Feature Engineering
- Label Encoding
- One-Hot Encoding
- Feature Scaling
- Logistic Regression
- Decision Trees
- Random Forest
- Cross Validation
- RandomizedSearchCV
- Hyperparameter Tuning
- Overfitting Detection
- Confusion Matrix
- Precision
- Recall
- F1-score
- ROC-AUC
- Model Evaluation

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# Future Improvements

Possible improvements for this project:

- Experiment with XGBoost, LightGBM, and CatBoost.
- Handle class imbalance using SMOTE or class weighting.
- Perform feature selection.
- Build a Streamlit web application.
- Deploy the model using cloud services.

---

# Learning Outcomes

This project helped me understand the complete machine learning workflow, from exploring real-world data and preprocessing it to training models, comparing algorithms, tuning hyperparameters, and selecting a final model based on appropriate evaluation metrics.

The project also highlights why metrics such as Precision, Recall, F1-score, and ROC-AUC are important when working with imbalanced classification problems.

---

## Author

Reevan Machado