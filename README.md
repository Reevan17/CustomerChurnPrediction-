# 📞 Telecom Customer Churn Prediction

An end-to-end **Machine Learning Classification** project that predicts whether a telecom customer is likely to **churn (leave the company)** or **stay**, based on customer demographics, subscription details, services used, contract type, and billing information.

This project is being built as a complete machine learning pipeline, covering everything from data exploration and preprocessing to model building, evaluation, hyperparameter tuning, and final model selection.

---

# 🎯 Project Goal

Customer retention is one of the biggest challenges for telecom companies. Acquiring a new customer is often significantly more expensive than retaining an existing one.

The goal of this project is to develop a machine learning model that predicts customer churn before it happens, enabling telecom companies to take proactive actions such as personalized offers, loyalty programs, and improved customer support to reduce customer attrition.

---

# 📌 Current Progress

- ✅ Exploratory Data Analysis (EDA)
- ✅ Data Preprocessing
- ✅ Baseline Model (Logistic Regression)
- ✅ Model Comparison
- ⏳ Hyperparameter Tuning
- ⏳ Final Model

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

Each row represents one telecom customer, and the objective is to predict whether the customer will churn or remain with the company.

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
- Customers with **month-to-month contracts** have the highest churn.
- **New customers** are more likely to churn.
- **Fiber optic** users have the highest churn rate.
- Customers paying through **electronic check** churn the most.
- Customers using **automatic payment methods** are less likely to churn.
- **Senior citizens** have a higher churn rate.
- **Gender** has little influence on churn.

---

# ⚙️ Data Preprocessing

The preprocessing pipeline included:

- Converted `TotalCharges` from `object` to numeric.
- Identified hidden missing values stored as blank strings.
- Removed rows with missing `TotalCharges`.
- Dropped the `customerID` column.
- Applied Label Encoding to binary categorical variables.
- Applied One-Hot Encoding to multi-category variables.
- Performed an 80:20 train-test split.
- Applied StandardScaler to numerical features.
- Saved the processed datasets for future model training.

---

# 🤖 Baseline Model (Logistic Regression)

| Metric | Score |
|---------|------:|
| Accuracy | **78.75%** |
| Precision | **62.06%** |
| Recall | **51.60%** |
| F1-Score | **56.35%** |
| ROC-AUC | **0.8319** |

The Logistic Regression model served as the baseline and demonstrated strong overall performance, particularly in terms of ROC-AUC and balanced classification performance.

---

# 📊 Model Comparison

Three machine learning algorithms were compared:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|---------:|----------:|--------:|---------:|--------:|
| Logistic Regression | **0.7875** | 0.6206 | 0.5160 | **0.5635** | **0.8319** |
| Decision Tree | 0.7335 | 0.4988 | **0.5481** | 0.5223 | 0.6739 |
| Random Forest | 0.7846 | **0.6300** | 0.4599 | 0.5317 | 0.8179 |

### Key Observations

- **Logistic Regression** achieved the highest overall performance based on **F1-Score** and **ROC-AUC**.
- **Decision Tree** achieved the highest recall but showed significant overfitting.
- **Random Forest** achieved the highest precision but missed more churning customers than Logistic Regression.
- Logistic Regression was selected as the strongest baseline model before hyperparameter tuning.

---

# 🎯 Hyperparameter Tuning

The next stage focuses on optimizing the best-performing models using:

- RandomizedSearchCV
- GridSearchCV *(optional)*

The goal is to reduce overfitting and improve churn prediction performance.

---

# 🏆 Final Model

The final notebook will include:

- Training the optimized model
- Final model evaluation
- Feature importance analysis
- Saving the trained model

---

# 🧠 Machine Learning Concepts Covered

- Binary Classification
- Exploratory Data Analysis (EDA)
- Data Cleaning
- Missing Value Handling
- Label Encoding
- One-Hot Encoding
- Feature Scaling
- Logistic Regression
- Decision Tree
- Random Forest
- Model Comparison
- Overfitting
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

- Hyperparameter tuning
- XGBoost implementation
- LightGBM and CatBoost comparison
- Handle class imbalance using SMOTE
- Build a Streamlit web application
- Deploy the trained model

---

# 📚 Learning Outcomes

This project demonstrates a complete machine learning classification workflow, including data exploration, preprocessing, feature engineering, baseline modeling, model comparison, and evaluation using business-focused metrics such as Precision, Recall, F1-Score, and ROC-AUC.

---

## 👨‍💻 Author

**Reevan Machado**