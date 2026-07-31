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
- ⏳ Model Comparison
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

The EDA focused on understanding customer behavior and identifying factors that influence churn.

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

# 🤖 Baseline Model

The first classification model built for this project is **Logistic Regression**, which serves as the baseline for comparing more advanced machine learning models.

## Baseline Model Performance

| Metric | Score |
|---------|------:|
| Accuracy | **79%** |
| Precision (Churn) | **62%** |
| Recall (Churn) | **52%** |
| F1-Score (Churn) | **56%** |
| ROC-AUC | **0.8319** |

### Key Observations

- The model achieved good overall accuracy (**79%**).
- It performs well in identifying customers who stay with the company.
- It detects approximately **52%** of customers who actually churn.
- The **ROC-AUC score of 0.8319** indicates a strong ability to distinguish between customers who churn and those who stay.
- This model serves as a benchmark for evaluating more advanced classification algorithms.

---

# 📊 Model Comparison

The following machine learning models will be compared:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier *(optional)*

Each model will be evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score

The best-performing model will be selected based on its ability to accurately identify customers at risk of churn.

---

# 🎯 Hyperparameter Tuning

The best-performing model from the comparison stage will be optimized using:

- RandomizedSearchCV
- GridSearchCV *(optional)*

The tuned model will then be evaluated on the test dataset to improve predictive performance.

---

# 🏆 Final Model

The final notebook will include:

- Training the optimized model
- Final model evaluation
- Feature importance analysis (if applicable)
- Saving the trained model for future predictions

---

# 🧠 Machine Learning Concepts Covered

- Binary Classification
- Exploratory Data Analysis (EDA)
- Data Cleaning
- Missing Value Handling
- Feature Engineering
- Label Encoding
- One-Hot Encoding
- Feature Scaling
- Logistic Regression
- Decision Trees
- Random Forest
- Hyperparameter Tuning
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

# 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Telecom-Churn-Prediction.git
```

### 2. Navigate to the project directory

```bash
cd Telecom-Churn-Prediction
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Run the notebooks in order

1. `01_EDA.ipynb`
2. `02_Data_Preprocessing.ipynb`
3. `03_Baseline_Model.ipynb`
4. `04_Model_Comparison.ipynb`
5. `05_Hyperparameter_Tuning.ipynb`
6. `06_Final_Model.ipynb`

---

# 🚀 Future Improvements

- Implement LightGBM and CatBoost models.
- Apply feature selection techniques.
- Address class imbalance using SMOTE.
- Optimize the decision threshold to improve churn detection.
- Build an interactive web application using Streamlit or Flask.
- Deploy the trained model to the cloud.
- Monitor model performance on new customer data.

---

# 📚 Learning Outcomes

This project demonstrates a complete end-to-end machine learning classification workflow, from understanding the business problem and exploring the dataset to preprocessing, model building, evaluation, and model optimization.

It also emphasizes interpreting model performance using business-focused metrics such as Precision, Recall, F1-Score, ROC Curve, and ROC-AUC, enabling data-driven decisions for improving customer retention.

---

## 👨‍💻 Author

**Reevan Machado**