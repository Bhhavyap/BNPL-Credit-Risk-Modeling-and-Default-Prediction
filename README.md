BNPL Credit Risk Modeling Project
End-to-end credit risk modeling project using BNPL data, focusing on default prediction, model evaluation, and business-driven decision making.

Overview
This project builds a credit risk model for a Buy Now Pay Later (BNPL) platform to predict customer default and support data-driven lending decisions. The objective is to identify high-risk customers, reduce potential losses, and improve portfolio quality using machine learning techniques.

Business Problem
BNPL platforms provide short-term unsecured credit, making them highly exposed to default risk. The key challenge is to accurately identify customers who are likely to default while minimizing rejection of creditworthy applicants.

Dataset Description
The dataset includes customer demographics, transaction details, repayment behavior, and engineered financial ratios.

Key Variables:
Customer Profile: age, employment_type, monthly_income
Creditworthiness: credit_score
Loan Details: purchase_amount, bnpl_installments
Behavioral Variables: repayment_delay_days, missed_payments
Financial Ratios: debt_to_income_ratio, loan_to_income
Target Variable: default_flag (1 = default, 0 = non-default)

Exploratory Data Analysis (EDA)
Key insights from the analysis:

Defaulters have significantly lower credit scores
Repayment delay is a strong indicator of default risk
Higher missed payments are associated with increased default probability
Higher loan-to-income ratios indicate financial stress and higher risk
Behavioral variables were found to be more predictive than demographic variables.

Feature Engineering
Created loan_to_income ratio to measure financial burden
Removed leakage variables such as risk_score and customer_segment

Model Development
Models Used:
Logistic Regression (Baseline)
Logistic Regression with Class Balancing
Random Forest Classifier

Model Evaluation
Logistic Regression (Balanced)
Recall (Default): 63%
Accuracy: 66%
Random Forest
Accuracy: 71%
Recall (Default): 48%

Model Selection

Although Random Forest achieved higher accuracy, it failed to detect a large number of defaulters.

The balanced Logistic Regression model was selected because:
It better identifies high-risk customers
It aligns with business objectives of minimizing credit losses

Key Insights
Repayment behavior is the strongest predictor of default
Credit score remains highly relevant
Financial burden (income & ratios) significantly impacts risk
Behavioral variables outperform demographic variables

Feature Importance (Random Forest)

Top predictors:

repayment_delay_days
credit_score
monthly_income
debt_to_income_ratio
loan_to_income

Confirms importance of behavioral and financial indicators

Conclusion

This project demonstrates how machine learning can be applied to credit risk modeling in BNPL lending. The results highlight the importance of behavioral signals and affordability metrics in predicting default risk. By aligning model performance with business objectives, the project provides a practical framework for improving lending decisions and reducing financial risk.

