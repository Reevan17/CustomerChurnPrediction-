# 📞 Telecom Customer Churn Prediction

An end-to-end **Machine Learning Classification** project that predicts whether a telecom customer is likely to **churn (leave the company)** or **stay**, based on customer demographics, subscription details, services used, contract type, and billing information.

This project follows a complete machine learning workflow, covering data exploration, preprocessing, model building, evaluation, hyperparameter tuning, and final model selection.

---

# 🎯 Project Goal

Customer retention is one of the biggest challenges for telecom companies. Acquiring a new customer is often significantly more expensive than retaining an existing one.

The goal of this project is to build a machine learning model that predicts customer churn in advance, allowing telecom companies to take proactive actions such as personalized offers, loyalty programs, and improved customer support to improve customer retention.

---

# 📌 Project Progress

- ✅ Exploratory Data Analysis (EDA)
- ✅ Data Preprocessing
- ✅ Baseline Model (Logistic Regression)
- ✅ Model Comparison
- ✅ Hyperparameter Tuning using RandomizedSearchCV
- ⏳ Final Model Selection & Deployment Preparation

---

# 📂 Project Structure

```text
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
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Data_Preprocessing.ipynb
│   ├── 03_Baseline_Model.ipynb
│   ├── 04_Model_Comparison.ipynb
│   ├── 05_Hyperparameter_Tuning.ipynb
│   └── 06_Final_Model.ipynb
│
├── models/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 📊 Dataset

- **Dataset:** Telco Customer Churn
- **Rows:** 7,043
- **Columns:** 21
- **Target Variable:** `Churn`

Each row represents one telecom customer, and the objective is to predict whether the customer will churn or continue using the service.

---

# 🔍 Exploratory Data Analysis (EDA)

### Analysis Performed

- Dataset overview
- Data type inspection
- Missing value analysis
- Duplicate check
- Target variable distribution
- Univariate analysis
- Bivariate analysis
- Business insights

### Key Findings

- Most customers remain with the company.
- The dataset has a moderate class imbalance:
  - No Churn: ~73%
  - Churn: ~27%
- Customers with **month-to-month contracts** have the highest churn.
- **New customers** are more likely to churn.
- **Fiber optic** users show higher churn rates.
- Customers paying through **electronic check** churn the most.
- Customers using **automatic payment methods** have lower churn.
- **Senior citizens** show a higher churn rate.
- **Gender** has little impact on churn.

---

# ⚙️ Data Preprocessing

The preprocessing pipeline included:

- Converted `TotalCharges` from object to numeric.
- Handled hidden missing values stored as blank strings.
- Removed rows with missing `TotalCharges`.
- Dropped unnecessary `customerID` column.
- Applied Label Encoding to binary categorical variables.
- Applied One-Hot Encoding to multi-category variables.
- Performed an 80:20 train-test split.
- Applied StandardScaler to numerical features.
- Saved processed datasets for model training.

---

# 🤖 Baseline Model (Logistic Regression)

Logistic Regression was used as the baseline classification model.

| Metric | Score |
|---------|------:|
| Accuracy | **78.75%** |
| Precision | **62.06%** |
| Recall | **51.60%** |
| F1-Score | **56.35%** |
| ROC-AUC | **83.19%** |

### Observation

The baseline model performed well despite the class imbalance, especially based on ROC-AUC and F1-score.

---

# 📊 Model Comparison

The following models were evaluated:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|---------:|----------:|--------:|---------:|--------:|
| Logistic Regression | **0.7875** | 0.6206 | **0.5160** | **0.5635** | **0.8319** |
| Decision Tree | 0.7335 | 0.4988 | **0.5481** | 0.5223 | 0.6739 |
| Random Forest | 0.7846 | **0.6300** | 0.4599 | 0.5317 | 0.8179 |

### Key Observations

- Logistic Regression achieved the best overall balance with the highest F1-score and ROC-AUC.
- Decision Tree showed strong recall but suffered from severe overfitting.
- Random Forest achieved better precision but lower recall compared to Logistic Regression.

---

# 🎯 Hyperparameter Tuning

Random Forest was optimized using **RandomizedSearchCV** with:

- 5-fold Cross Validation
- F1-score as the optimization metric
- Random search over multiple hyperparameter combinations

### Best Hyperparameters

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

# 📈 Tuned Random Forest Performance

| Metric | Score |
|---------|------:|
| Accuracy | **79.46%** |
| Precision | **65.68%** |
| Recall | **47.59%** |
| F1-Score | **55.19%** |
| ROC-AUC | **83.16%** |

---

# 🔍 Overfitting Reduction

Before tuning:

| Model | Training Accuracy | Testing Accuracy |
|-------|------------------:|-----------------:|
| Random Forest | 99.77% | 78.46% |

After tuning:

| Model | Training Accuracy | Testing Accuracy |
|-------|------------------:|-----------------:|
| Tuned Random Forest | 84.99% | 79.46% |

### Observation

Hyperparameter tuning significantly reduced overfitting by limiting tree complexity while maintaining strong performance on unseen data.

---

# 🏆 Final Model

The final notebook will include:

- Comparing Logistic Regression and Tuned Random Forest.
- Selecting the final model based on evaluation metrics.
- Training the selected model.
- Saving the trained model using Joblib.
- Testing predictions on new customer data.

---

# 🧠 Machine Learning Concepts Covered

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
- Model Comparison
- Cross Validation
- RandomizedSearchCV
- Hyperparameter Tuning
- Overfitting Detection
- Confusion Matrix
- Precision
- Recall
- F1-Score
- ROC Curve
- ROC-AUC
- Model Evaluation

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 🚀 Future Improvements

- Implement XGBoost, LightGBM, and CatBoost.
- Experiment with class imbalance techniques such as SMOTE and class weighting.
- Perform feature selection.
- Build an interactive churn prediction application using Streamlit.
- Deploy the model using cloud services.

---

# 📚 Learning Outcomes

This project demonstrates a complete machine learning classification pipeline, from understanding the business problem and exploring customer behavior to preprocessing data, building classification models, optimizing performance, and selecting a final model using data-driven evaluation.

The project also highlights the importance of choosing appropriate evaluation metrics for imbalanced datasets instead of relying only on accuracy.

---

## 👨‍💻 Author

**Reevan Machado**