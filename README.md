#  Random Forest – Credit Card Fraud Detection

## 📌 Project Overview

This project focuses on building a **machine learning-based fraud detection system** to identify fraudulent transactions from highly imbalanced transaction data.
Implemented and compared **Logistic Regression (baseline model)** and **Random Forest (advanced model)** to evaluate performance and select the best model.

##  Objective

* Detect fraudulent transactions accurately
* Handle highly imbalanced dataset
* Compare baseline and advanced ML models
* Optimize fraud detection using evaluation metrics such as Precision, Recall, and F1-score
* Save trained model for reuse

##  Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Joblib

##  Dataset Information

**Dataset Name:** Credit Card Fraud Dataset (Kaggle)

* Total Records: 284,807
* Fraud Transactions: 492
* Non-Fraud Transactions: 284,315
* Target Column: `Class`

  * 0 → Non-Fraud
  * 1 → Fraud

##  Project Workflow

###  Data Loading & Exploration

* Loaded dataset using Pandas
* Checked dataset shape and structure
* Analyzed class imbalance between fraud and non-fraud transactions

### 2️ Data Preprocessing

* Separated features and target column
* Removed non-useful columns
* Applied StandardScaler for Logistic Regression model

###  Train-Test Split

* Used stratified sampling
* Maintained fraud ratio in both training and testing datasets
* Split ratio: 80% training and 20% testing

###  Baseline Model: Logistic Regression

* Used Logistic Regression as baseline model
* Applied feature scaling
* Used `lbfgs` solver and increased iterations for stable convergence
* Evaluated using precision, recall, and F1-score

###  Advanced Model: Random Forest

* Trained Random Forest Classifier with 100 trees
* Achieved improved fraud detection performance
* No scaling required for tree-based model

###  Model Evaluation

Since the dataset is highly imbalanced, accuracy was not considered reliable.

Main evaluation metrics used:

* Precision
* Recall
* F1-score
* Confusion Matrix

###  Feature Importance Analysis

* Extracted feature importance from Random Forest
* Visualized top contributing features
* Identified important fraud indicators

###  Model Comparison

| Model               | Precision | Recall | F1-Score |
| ------------------- | --------- | ------ | -------- |
| Logistic Regression | 0.84      | 0.61   | 0.71     |
| Random Forest       | 0.95      | 0.83   | 0.89     |

###  Model Saving

* Best performing model (Random Forest) is saved using Joblib
  
---
