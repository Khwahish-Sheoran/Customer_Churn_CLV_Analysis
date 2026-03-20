# Customer-Churn-CLV-Analysis
Problem Statement

The objective of this project is to predict customer churn and identify high-value customers who are at risk of leaving. The goal is to move beyond simple prediction and build a system that helps prioritize customers for retention based on both their churn probability and economic value.

Dataset

The dataset used is the Telco Customer Churn dataset from Kaggle. It contains customer-level information such as demographics, contract details, tenure, and billing information.

Methodology

1. Data Preprocessing

Converted relevant columns to appropriate data types

Handled missing values in TotalCharges

Encoded categorical variables using one-hot encoding

Removed non-informative features such as customerID

2. Exploratory Data Analysis

Analyzed class imbalance in churn

Studied the relationship between churn and features such as contract type, tenure, and monthly charges

Identified patterns indicating that shorter contracts and higher charges are associated with higher churn

3. Model Development

Implemented Logistic Regression and Random Forest models

Evaluated models using accuracy, classification report, and ROC-AUC

Selected Random Forest as the final model based on performance

4. Model Interpretation

Used SHAP values to understand feature importance

Identified key drivers of churn such as contract type, monthly charges, and tenure

5. Customer Lifetime Value (CLV)

Estimated CLV as a proxy using monthly charges multiplied by tenure

Used this as a measure of customer importance

6. Customer Segmentation

Combined churn probability with CLV to create actionable customer segments

Segments include:

High Risk – High Value

High Risk – Low Value

Low Risk – High Value

Low Risk – Low Value

7. Priority Scoring

Created a priority score defined as:
Priority Score = Churn Probability × CLV

This allows ranking customers based on both risk and value

Results

The Random Forest model achieved strong predictive performance in identifying churn

SHAP analysis confirmed that contract type, monthly charges, and tenure are the most important factors

A distinct group of high-value customers at risk of churn was identified

Key Insights

Customers on month-to-month contracts have significantly higher churn rates

Higher monthly charges are associated with increased churn probability

Customers with longer tenure are less likely to churn

Not all high-risk customers are equally important; prioritization based on value is necessary

Business Implications

Retention efforts should focus on high-risk, high-value customers

Pricing strategies and contract structures play an important role in churn

A targeted approach can reduce unnecessary retention costs

Tech Stack

Python

Pandas, NumPy

Scikit-learn

SHAP

Matplotlib, Seaborn
