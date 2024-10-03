# Bankruptcy_Prediction Using Machine Learning 
This repository contains the code and resources for a Bankruptcy Prediction project aimed at forecasting the financial insolvency of publicly traded U.S. companies using machine learning algorithms. The project leverages historical financial data spanning nearly two decades (1999-2018) to build models that assist in identifying companies at risk of bankruptcy. The predictions can help investors, creditors, and regulators to make informed decisions.

<h3>Background</h3>
Bankruptcy prediction is vital for stakeholders such as investors, creditors, and regulatory agencies. Traditional methods relied heavily on financial ratios and expert opinions, but the rise of big data and machine learning offers an opportunity to improve prediction accuracy. This project seeks to address the challenges of non-linear financial data relationships and class imbalance using advanced algorithms.

<h3>Project Objective</h3>
The main goal of this project is to create a machine learning model capable of predicting corporate bankruptcies based on historical financial indicators. The project uses a dataset sourced from Kaggle and applies various machine learning techniques to create a predictive model. Key questions addressed include:
<ol>
  <li>Which financial indicators are the most predictive of bankruptcy?</li>
  <li>How can we manage the class imbalance between bankrupt and non-bankrupt companies?</li>
  <li>Which model performs best in terms of prediction accuracy?</li>
  <li>How can the model’s results be made interpretable for stakeholders?</li>
</ol>

<h3Dataset Overview</h3>
<ul>
<li><strong>Time Period:</strong>999-2018</li>
<li><strong>Records:</strong> 78,682 rows</li>
<li><strong>Columns:</strong> 21 (including financial indicators such as market value, total liabilities, and net income)</li>
<li><strong>Target Variable:</strong> status_label (binary classification: bankrupt or non-bankrupt)</li>
</ul>

<h3>Models Used</h3>
The following machine learning models were evaluated for performance:

<ol>
<li><b>Logistic Regression</b> - Poor recall and precision, especially for the minority class.</li>
<li><b>Decision Tree</b> - Better recall than logistic regression but still prone to false positives.</li>
<li><b>Random Forest</b> - Best overall model with the highest accuracy (93.66%) and balanced precision-recall performance.</li>
<li><b>Gradient Boosting</b> - Competitive accuracy but lower recall for the minority class.</li>
<li><b>XGBoost</b> - Best recall for minority class (49.13%), making it highly useful for detecting at-risk companies.</li>
</ol>

<h3>Final Model</h3>
The project combined <strong>Random Forest</strong> and <strong>XGBoost</strong> to leverage the strengths of both:

<ul>
<li><b>Random Forest</b> for stability and high overall accuracy.</li>
<li><b>XGBoost</b> for better detection of bankrupt companies (minority class).</li>
</ul>

<h3>Key Features Selected</h3>

<ul>
<li>Market Value</li>
<li>Net Income</li>
<li>Retained Earnings</li>
<li>Total Liabilities</li>
<li>Depreciation & Amortization</li>
</ul>

<h3>Data Preprocessing</h3>
<li><b>Standardization:</b> Used StandardScaler to normalize numerical features.</li>
<li><b>Feature Selection:</b> Applied Random Forest to reduce the dataset to the most important financial indicators.</li>
<li><b>Handling Class Imbalance:</b> Used Synthetic Minority Oversampling Technique (SMOTE) to address the imbalance between bankrupt and non-bankrupt companies.</li>

<h3>Performance Metrics</h3>

<ul>
<li><b>Accuracy:</b> 93.66% (Random Forest)</li>
<li><b>Recall (minority class):</b> 49.13% (XGBoost)</li>
<li><b>F1-Score:</b> 97.65% (Random Forest for non-bankrupt companies)</li>
<li><b>AUC ROC:</b> 0.8422 (Random Forest)</li>
<li><b>MAE:</b> 7% for Random Forest</li>
</ul>

<h3>Visualizations</h3>

<ul>
<li><strong>Lift Charts</strong> and <strong>Gain Charts</strong> were used to evaluate model performance across deciles.</li>
<li><strong>Correlation Matrix<strong> to understand financial interdependencies.</li>
<li><strong>Pair Plots</strong> to visualize the separation between bankrupt and non-bankrupt companies.</li>
</ul>
