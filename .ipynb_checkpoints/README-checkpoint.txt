Customer Churn Prediction
Project Description
Beta-Bank has been experiencing customer churn. Every month, a noticeable number of customers leave the bank. Marketing analysis indicates that retaining current customers is more cost-effective than acquiring new ones. The objective is to predict whether a customer will leave the bank in the near future using historical data on customer behavior and account terminations.

The goal is to develop a model with a high F1 score. The project is considered successful if the F1 score reaches at least 0.59. Additionally, the AUC-ROC metric should be measured and compared with the F1 score.

Data Description
File: /datasets/Churn.csv

Features
RowNumber — row index in the data
CustomerId — unique customer identifier
Surname — surname
CreditScore — credit score
Geography — country of residence
Gender — gender
Age — age
Tenure — number of years the customer has been with the bank
Balance — account balance
NumOfProducts — number of bank products used by the customer
HasCrCard — credit card possession
IsActiveMember — customer activity status
EstimatedSalary — estimated salary
Target Feature
Exited — customer churn indicator
Project Evaluation Criteria
Reviewers will assess the project based on the following criteria:

Data Preparation
Handling of all feature types.
Preprocessing Steps
Clarity of preprocessing steps.
Class Balance Analysis
Exploration of class balance.
Data Splitting
Correct data splitting techniques.
Handling Class Imbalance
Proper training, validation, and testing of the model.
Metrics
Achieved F1 score.
AUC-ROC value.