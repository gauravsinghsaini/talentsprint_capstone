# Employee Attrition Prediction Analysis

## 1. Overview
This project focuses on identifying the primary factors contributing to employee attrition and building a predictive model to identify at-risk employees. By analyzing a dataset of 1,470 employee records, we explore demographic, professional, and satisfaction-related variables to understand why employees leave an organization.

## 2. Dataset
The analysis uses the **IBM HR Analytics Employee Attrition & Performance** dataset. 
*   **Source:** [Kaggle - Employee Attrition](https://www.kaggle.com/datasets/patelprashant/employee-attrition)
*   **Initial Structure:** 1,470 rows and 35 columns.
*   **Target Variable:** `Attrition` (Yes/No).

## 3. Technologies Used
The project is implemented in Python within a Google Colab environment using the following libraries:
*   **Data Manipulation:** `pandas`, `numpy`.
*   **Visualization:** `matplotlib`, `seaborn`.
*   **Machine Learning:** `scikit-learn` (Preprocessing, Modeling, Hyperparameter Tuning).

## 4. Methodology
### 4.1 Data Cleaning
Four non-informative or zero-variance columns were removed to optimize the models:
*   `EmployeeCount`, `EmployeeNumber`, `Over18`, and `StandardHours`.

### 4.2 Exploratory Data Analysis (EDA)
Key findings from the EDA phase include:
*   **Overtime:** Employees working overtime are significantly more likely to leave.
*   **Job Satisfaction:** A clear inverse relationship between satisfaction scores and attrition rates.
*   **Departmental Trends:** The Sales department exhibited higher attrition compared to Research & Development.

### 4.3 Preprocessing
*   **Encoding:** Categorical variables were transformed using `OneHotEncoder` (drop='first').
*   **Scaling:** Numerical features were standardized using `StandardScaler`.
*   **Splitting:** The data was split into training (80%) and testing (20%) sets.

## 5. Model Performance
Three classification models were compared:

| Model | Accuracy |
| :--- | :--- |
| **Random Forest Classifier** | **86.05%** |
| **Logistic Regression** | 83.67% |
| **Support Vector Machine (SVM)** | 83.33% |

## 6. Optimization
A `RandomizedSearchCV` was performed on the Logistic Regression model to find the best hyperparameters, resulting in a model using a `liblinear` solver and `l1` penalty.

## 7. Future Enhancements
*   Address the class imbalance (84/16 split) using techniques like SMOTE (Synthetic Minority Over-sampling Technique).
*   Explore advanced boosting algorithms such as XGBoost or LightGBM.

## 8. How to Run
1.  Clone this repository.
2.  Set up your Kaggle API credentials to download the dataset.
3.  Open the `.ipynb` notebook in Google Colab or Jupyter.
4.  Execute the cells in sequence.

---
**Author:** Gaurav Singh Saini  
**Date:** April 16, 2026
