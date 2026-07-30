# 📞 Telecom Customer Churn Prediction

An end-to-end **Machine Learning Classification** project that predicts whether a telecom customer is likely to **churn (leave the company)** or **stay**, based on customer demographics, subscription details, services used, contract type, and billing information.

This project follows a complete machine learning workflow, including **Exploratory Data Analysis (EDA)**, **Data Preprocessing**, **Model Building**, **Model Comparison**, **Hyperparameter Tuning**, and **Final Model Evaluation**.

---

# 🎯 Project Goal

Customer retention is one of the biggest challenges for telecom companies. Acquiring a new customer is often more expensive than retaining an existing one.

The goal of this project is to build a machine learning model that predicts customer churn in advance so that businesses can proactively retain at-risk customers through targeted offers, improved customer support, and personalized retention strategies.

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

* **Dataset:** Telco Customer Churn
* **Rows:** 7,043
* **Columns:** 21
* **Target Variable:** `Churn`

Each record represents one telecom customer, and the objective is to predict whether the customer will churn.

---

# 🔍 Exploratory Data Analysis (EDA)

The EDA focused on understanding customer behavior and identifying patterns associated with churn.

### Analysis Performed

* Dataset overview
* Data type inspection
* Missing value analysis
* Duplicate check
* Target variable distribution
* Univariate analysis
* Bivariate analysis
* Business insights

### Key Findings

* Most customers remain with the company.
* Customers with **month-to-month contracts** have the highest churn.
* **New customers** are more likely to churn.
* **Fiber optic** users have the highest churn rate.
* Customers paying through **electronic check** churn the most.
* Customers using **automatic payment methods** are less likely to churn.
* **Senior citizens** show a higher churn rate.
* **Gender** has little influence on churn.

---

# ⚙️ Data Preprocessing

The preprocessing pipeline included:

* Converted `TotalCharges` from `object` to numeric.
* Identified hidden missing values stored as blank strings.
* Removed rows with missing `TotalCharges`.
* Dropped the `customerID` column.
* Applied **Label Encoding** to binary categorical features.
* Applied **One-Hot Encoding** to multi-category features.
* Performed an 80:20 train-test split.
* Applied **StandardScaler** to numerical features.
* Saved the processed datasets for model training.

---

# 🤖 Model Building

## Baseline Model

* Logistic Regression

Evaluation Metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC Score

---

# 📊 Model Comparison

The following classification models are compared:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* XGBoost Classifier *(optional)*

The best-performing model is selected based on evaluation metrics.

---

# 🎯 Hyperparameter Tuning

Model performance is improved using:

* RandomizedSearchCV
* GridSearchCV *(optional)*

The tuned model is then evaluated on the test dataset.

---

# 🏆 Final Model

The final notebook includes:

* Training the optimized model
* Model evaluation
* Feature importance analysis (if applicable)
* Saving the trained model for future predictions

---

# 🧠 Machine Learning Concepts Covered

* Binary Classification
* Exploratory Data Analysis (EDA)
* Data Cleaning
* Missing Value Handling
* Feature Engineering
* Label Encoding
* One-Hot Encoding
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
* ROC-AUC
* Model Evaluation

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# 🚀 How to Run

1. Clone this repository.

```bash
git clone https://github.com/your-username/Telecom-Churn-Prediction.git
```

2. Install the required libraries.

```bash
pip install -r requirements.txt
```

3. Open the notebooks in Jupyter Notebook or VS Code.

4. Run the notebooks in order:

* 01_EDA.ipynb
* 02_Data_Preprocessing.ipynb
* 03_Baseline_Model.ipynb
* 04_Model_Comparison.ipynb
* 05_Hyperparameter_Tuning.ipynb
* 06_Final_Model.ipynb

---

# 🚀 Future Improvements

* Implement LightGBM and CatBoost models.
* Apply feature selection techniques.
* Address class imbalance using SMOTE.
* Build an interactive web application using Streamlit or Flask.
* Deploy the trained model to the cloud.
* Monitor model performance on new customer data.

---

# 📚 Learning Outcomes

This project demonstrates a complete end-to-end machine learning classification pipeline. It covers the entire workflow from understanding the business problem and exploring the dataset to preprocessing, model building, hyperparameter tuning, and performance evaluation. It also emphasizes translating data insights into actionable business strategies for improving customer retention.

---

## 👨‍💻 Author

**Reevan Machado**
