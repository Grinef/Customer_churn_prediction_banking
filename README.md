# Customer Churn Prediction

## Project Overview

Beta-Bank has been facing customer churn, with a noticeable number of customers leaving the bank each month. According to marketing analysis, retaining existing customers is more cost-effective than acquiring new ones. The objective of this project is to develop a model that predicts whether a customer will leave the bank in the near future based on historical data about customer behavior and account terminations.

**Project Goals:**

- Develop a classification model to predict customer churn.
- Achieve a minimum F1 score of 0.59 on the test dataset.
- Additionally, measure the AUC-ROC metric and compare it with the F1 score.

## Features Description

The dataset contains the following features:

- **RowNumber**: Row index in the data.
- **CustomerId**: Unique customer identifier.
- **Surname**: Customer's surname.
- **CreditScore**: Customer's credit score.
- **Geography**: Customer's country of residence.
- **Gender**: Customer's gender.
- **Age**: Customer's age.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Customer's account balance.
- **NumOfProducts**: Number of bank products used by the customer.
- **HasCrCard**: Indicator if the customer has a credit card.
- **IsActiveMember**: Indicator of the customer's activity status.
- **EstimatedSalary**: Estimated salary of the customer.

**Target Feature:**

- **Exited**: Customer churn indicator (1 if the customer left, 0 if they stayed).

## Data Preprocessing and Analysis

The data was preprocessed and analyzed, leading to the following key insights:

- **Missing Values**: Missing values were detected in the "Tenure" field. After analysis, these were replaced with "-1".
- **Duplicates**: No duplicate records were found.
- **Outliers and Anomalies**: No significant outliers or anomalies were detected in the data.
- **Multicollinearity**: No multicollinearity was found among the features.
- **Class Imbalance**: The target variable exhibited class imbalance, which was addressed during model training.
- **Categorical Features Encoding**: Categorical features were encoded using dummy variables due to the small number of categories in each feature.

## Modeling and Results

Several models were developed and evaluated, with the following outcomes:

- **Baseline Model**: Logistic Regression was used as the baseline model but did not meet the minimum quality threshold.
- **Final Model**: A RandomForestClassifier with tuned hyperparameters was selected as the final model.

### Additional Metrics for Quality Control:

1. GINI
2. ROC-AUC
3. Confusion Matrix

### Final Model Performance:

- **Ranking Ability**:
  - GINI on DEV set: 0.76
  - GINI on VAL (test) set: 0.71
  - Relative change in GINI: -0.06
  - Area under ROC Curve: 0.86
- **Model Accuracy**:
  - F1 score on DEV set: 0.63
  - F1 score on VAL (test) set: 0.60
  - Relative change in F1 score: -0.05
- **Confusion Matrix Analysis**:
  - **True Positive (TP)**: 1332 — The model correctly predicted 1332 cases as positive.
  - **False Negative (FN)**: 271 — The model incorrectly predicted 271 positive cases as negative.
  - **False Positive (FP)**: 118 — The model incorrectly predicted 118 negative cases as positive.
  - **True Negative (TN)**: 289 — The model correctly predicted 289 cases as negative.

Detailed results, including the ROC Curve, are illustrated in the file: `ROC_AUC_FINALLY_Model.png`.

## Conclusion

The objectives set by the client have been successfully achieved. The final model meets the required performance metrics and is ready for deployment.
