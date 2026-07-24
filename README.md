# Employee Attrition Prediction using Machine Learning

## Project Overview

Employee attrition refers to employees leaving an organization. High attrition can increase recruitment costs and reduce productivity. This project uses Machine Learning to predict whether an employee is likely to leave the company based on personal and job-related information.

---

## Problem Statement

The objective of this project is to build a classification model that predicts employee attrition and identifies the factors that contribute to employees leaving the organization.

---

## Dataset Information

- Dataset: IBM HR Analytics Employee Attrition Dataset
- Total Records: 1,470
- Total Features: 35
- Target Variable: `Attrition`

### Target Classes

- **Yes** → Employee left the company
- **No** → Employee stayed with the company

### Class Distribution

| Attrition | Percentage |
|-----------|-----------:|
| No | 83.88% |
| Yes | 16.12% |

The dataset is imbalanced because most employees did not leave the company.

---

## Project Workflow

```text
Dataset
   ↓
Data Exploration
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Encoding
   ↓
Feature Scaling
   ↓
Train Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
```

---

## Data Preprocessing

The following preprocessing steps were performed:

- Checked data types
- Verified missing values
- Checked duplicate records
- Converted the target variable into numeric values
- Removed unnecessary columns:
  - EmployeeCount
  - EmployeeNumber
  - Over18
  - StandardHours
- Encoded categorical variables
- Applied One Hot Encoding using `pd.get_dummies()`
- Converted boolean columns into integers

---

## Exploratory Data Analysis (EDA)

The following visualizations were created:

- Attrition Distribution
- Age vs Attrition
- Monthly Income vs Attrition
- Overtime vs Attrition

Correlation analysis was also performed to identify the most important numerical features related to employee attrition.

---

## Feature Engineering

### Label Encoding

Applied to:

- Attrition
- Gender
- OverTime

### One Hot Encoding

Applied to:

- Department
- BusinessTravel
- MaritalStatus
- EducationField
- JobRole

---

## Feature Scaling

StandardScaler was applied before training Logistic Regression.

```python
scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

---

## Machine Learning Models

Three classification models were trained:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Classification Report

---

## Model Performance

| Model | Accuracy | Recall | F1 Score |
|-------|---------:|-------:|---------:|
| Logistic Regression | 71.77% | 58.97% | 35.66% |
| Random Forest | 87.41% | 12.82% | 21.28% |
| XGBoost | **88.44%** | 30.77% | **41.38%** |

---

## Best Model

**XGBoost** achieved the best overall performance.

- Accuracy: **88.44%**
- Precision: **63.16%**
- Recall: **30.77%**
- F1 Score: **41.38%**

---

## Key Findings

- Employees who work overtime are more likely to leave.
- Monthly income has an impact on attrition.
- Total working years and job level show a noticeable relationship with employee attrition.
- The dataset is imbalanced, which affects recall and F1 score.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

## Project Structure

```text
Employee-Attrition-Prediction/
│
├── Employee_Attrition_Prediction.ipynb
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Handle class imbalance using SMOTE.
- Perform Hyperparameter Tuning using GridSearchCV.
- Apply Cross Validation.
- Train additional models such as SVM and KNN.
- Deploy the model using Streamlit.

---

## Conclusion

This project successfully predicts employee attrition using Machine Learning. Three classification models were compared, and XGBoost achieved the best performance. The project demonstrates a complete machine learning workflow, including data preprocessing, exploratory data analysis, feature engineering, model training, and performance evaluation.

---

## Author

**Zain**

BS Computer Science

Machine Learning and Data Science
