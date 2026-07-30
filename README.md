# Telecom Customer Churn Prediction

A complete **Machine Learning Classification** project that predicts whether a telecom customer is likely to **churn (leave the company)** or **stay** based on customer demographics, services, account information, and billing details.

This project follows an end-to-end machine learning workflow, including **Exploratory Data Analysis (EDA)**, **Data Preprocessing**, **Model Building**, **Model Comparison**, **Hyperparameter Tuning**, and **Final Model Evaluation**.

---

# 📌 Project Goal

The objective of this project is to help a telecom company identify customers who are at risk of leaving. By predicting customer churn in advance, businesses can take proactive measures such as personalized offers, loyalty programs, and improved customer support to increase customer retention.

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
└── requirements.txt
```

---

# 📊 Dataset

* **Dataset:** Telco Customer Churn
* **Rows:** 7,043
* **Columns:** 21
* **Target Variable:** `Churn`

Each row represents one telecom customer, and the goal is to predict whether the customer will leave the company.

---

# 🛠️ Project Workflow

## 1. Exploratory Data Analysis (EDA)

* Dataset overview
* Missing value analysis
* Duplicate check
* Target variable analysis
* Univariate analysis
* Bivariate analysis
* Business insights

### Key Findings

* Most customers do not churn.
* New customers have a higher churn rate.
* Month-to-month contracts show the highest churn.
* Fiber optic customers churn more than other internet service users.
* Electronic check users have the highest churn.
* Automatic payment users have lower churn.
* Senior citizens churn more frequently.
* Gender has little impact on churn.

---

## 2. Data Preprocessing

* Handle incorrect data types
* Convert `TotalCharges` to numeric
* Handle hidden missing values
* Drop unnecessary columns
* Encode categorical variables
* Train-test split
* Save processed dataset

---

## 3. Baseline Model

Train the first classification model using:

* Logistic Regression

Evaluation metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

---

## 4. Model Comparison

Models compared:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* (Optional) XGBoost Classifier

Performance comparison helps identify the best-performing model.

---

## 5. Hyperparameter Tuning

Improve the selected model using:

* RandomizedSearchCV
* GridSearchCV (optional)

---

## 6. Final Model

* Train the optimized model
* Evaluate performance
* Save the trained model for future predictions

---

# 📈 Machine Learning Concepts Covered

* Binary Classification
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Label Encoding
* One-Hot Encoding
* Data Cleaning
* Feature Scaling
* Logistic Regression
* Decision Trees
* Random Forest
* Hyperparameter Tuning
* Confusion Matrix
* Precision
* Recall
* F1-Score
* ROC Curve
* Model Evaluation

---

# 🧰 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# 🚀 Future Improvements

* Implement XGBoost and LightGBM
* Perform feature selection
* Handle class imbalance using SMOTE
* Build an interactive churn prediction web application using Flask or Streamlit
* Deploy the trained model to the cloud

---

# 📚 Learning Outcomes

This project demonstrates a complete machine learning classification pipeline, from understanding business requirements and exploring data to building, tuning, and evaluating predictive models. It also emphasizes converting data insights into actionable business recommendations for improving customer retention.

---

**Author:** Reevan Machado
