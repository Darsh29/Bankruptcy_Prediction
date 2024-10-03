# Bankruptcy_Prediction Using Machine Learning 
This repository contains the code and resources for a Bankruptcy Prediction project aimed at forecasting the financial insolvency of publicly traded U.S. companies using machine learning algorithms. The project leverages historical financial data spanning nearly two decades (1999-2018) to build models that assist in identifying companies at risk of bankruptcy. The predictions can help investors, creditors, and regulators to make informed decisions.

<H3>Background</H3>
Bankruptcy prediction is vital for stakeholders such as investors, creditors, and regulatory agencies. Traditional methods relied heavily on financial ratios and expert opinions, but the rise of big data and machine learning offers an opportunity to improve prediction accuracy. This project seeks to address the challenges of non-linear financial data relationships and class imbalance using advanced algorithms.

Project Objective
The main goal of this project is to create a machine learning model capable of predicting corporate bankruptcies based on historical financial indicators. The project uses a dataset sourced from Kaggle and applies various machine learning techniques to create a predictive model. Key questions addressed include:

Which financial indicators are the most predictive of bankruptcy?
How can we manage the class imbalance between bankrupt and non-bankrupt companies?
Which model performs best in terms of prediction accuracy?
How can the model’s results be made interpretable for stakeholders?
Dataset Overview
Source: Kaggle
Time Period: 1999-2018
Records: 78,682 rows
Columns: 21 (including financial indicators such as market value, total liabilities, and net income)
Target Variable: status_label (binary classification: bankrupt or non-bankrupt)
Models Used
The following machine learning models were evaluated for performance:

Logistic Regression - Poor recall and precision, especially for the minority class.
Decision Tree - Better recall than logistic regression but still prone to false positives.
Random Forest - Best overall model with the highest accuracy (93.66%) and balanced precision-recall performance.
Gradient Boosting - Competitive accuracy but lower recall for the minority class.
XGBoost - Best recall for minority class (49.13%), making it highly useful for detecting at-risk companies.
Final Model
The project combined Random Forest and XGBoost to leverage the strengths of both:

Random Forest for stability and high overall accuracy.
XGBoost for better detection of bankrupt companies (minority class).
Key Features Selected
Market Value
Net Income
Retained Earnings
Total Liabilities
Depreciation & Amortization
Data Preprocessing
Standardization: Used StandardScaler to normalize numerical features.
Feature Selection: Applied Random Forest to reduce the dataset to the most important financial indicators.
Handling Class Imbalance: Used Synthetic Minority Oversampling Technique (SMOTE) to address the imbalance between bankrupt and non-bankrupt companies.
Performance Metrics
Accuracy: 93.66% (Random Forest)
Recall (minority class): 49.13% (XGBoost)
F1-Score: 97.65% (Random Forest for non-bankrupt companies)
AUC ROC: 0.8422 (Random Forest)
MAE: 7% for Random Forest
Visualizations
Lift Charts and Gain Charts were used to evaluate model performance across deciles.
Correlation Matrix to understand financial interdependencies.
Pair Plots to visualize the separation between bankrupt and non-bankrupt companies.
