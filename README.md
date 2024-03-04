# 20-credit-risk-classification

## Overview of the Analysis

The purpose of this analysis was to develop a machine learning model capable of predicting the creditworthiness of borrowers for a peer-to-peer lending services company. By utilizing historical lending activity data, the goal was to classify loans as either "healthy" (0) or "high-risk" (1) of defaulting, aiding in the decision-making process for loan approval.

The dataset comprised various financial attributes of borrowers, including loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and the loan status (healthy or high-risk). The primary task was to predict the "loan_status" variable based on these features.

### Process 
The machine learning process involved several key stages:

- Data preparation, including reading the data, creating features (X) and labels (y), and splitting the dataset into 80% training and 20% testing sets.
- Model training using a logistic regression classifier, followed by making predictions and evaluating model performance.
- Addressing class imbalance through resampling techniques, specifically using RandomOverSampler, and re-evaluating the model's performance on the balanced dataset.

### Results

The analysis involved two main logistic regression models:

Machine Learning Model 1 (Original Data):
 - Balanced Accuracy Score: 0.9669
 - Precision for Healthy Loans (0): 1.00
 - Precision for High-Risk Loans (1): 0.86
 - Recall for Healthy Loans (0): 0.99
 - Recall for High-Risk Loans (1): 0.94
<br>

Machine Learning Model 2 (Resampled Data):
 - Balanced Accuracy Score: 0.9941
 - Precision for Healthy Loans (0): 1.00
 - Precision for High-Risk Loans (1): 0.85
 - Recall for Healthy Loans (0): 0.99
 - Recall for High-Risk Loans (1): 0.99

### Summary

Comparing the two models, Machine Learning Model 2, which utilized resampled data to correct for class imbalance, exhibited superior overall performance. The improvement in balanced accuracy from 0.9669 to 0.9941 highlights the effectiveness of addressing class imbalance in enhancing model reliability across both classes. The recall improvement for high-risk loans in Model 2 emphasizes its utility in accurately identifying high-risk borrowers, which is paramount for reducing default risks.

Given the objective of accurately identifying both healthy and high-risk loans, Model 2's enhanced recall for high-risk loans without a substantial compromise in precision makes it the recommended model for deployment. Its outstanding performance underscores the importance of addressing class imbalance in datasets to improve model accuracy and reliability in real-world applications.

### Conclusion
In conclusion, while both models exhibit strong predictive capabilities, the resampled logistic regression model (Model 2) is recommended for its exceptional balance between precision and recall, especially in predicting high-risk loans. This model offers a more reliable tool for assessing loan applications, ultimately aiding in risk management and decision-making processes for the lending company.
 
