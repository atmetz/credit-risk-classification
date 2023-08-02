# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to attempt to predict the creditworthiness of potential borrowers.
This used historical lending activity including the requested loan amount, interest rate, borrower's income, debt to income ration, number of accounts, derogatory marks, and total debt.
The model is attempting to predict if the borrow is a high risk of defaulting on the loan.
The data set had 75,036 healthy loans and 2500 high risk loans. For machine learning, I seperated out the features(loan amount, interest rate, borrower's income, debt to income ration, number of accounts, derogatory marks, and total debt)
and the target (loan status). From here, I used train_test_split to get the training data(X_train, y_train) and the test data(X_test, y_test). From here, X_train and y_train were fit to a LogisticRegression model, and predictions were made with the X_test data. The predictions were compared against the y_test data to score how well the model performed.
Since the amount of healthy loans was significantly higher than the high risk loans, the model was able to get 100% on the healthy loans, but only 87% of the high risk loans.
Next, RandomOverSampler was used to make the two outcomes have an even number of results. A LogisticRegression was used using this new data, resulting in 90% of healthy loans and 99% of high risk loans identified.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model (LogisticRegression):
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Accuracy: 99%
  * Precision: 100% Healthy Loans, 87% High Risk Loans
  * Recall: 100% Healthy Loans, 89% High Risk Loans



* Machine Learning Model (RandomOverSampler LogisticRegression):
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Accuracy: 94%
  * Precision: 90% Healthy Loans, 99% High Risk Loans
  * Recall: 99% Healthy Loans, 89% High Risk Loans

## Summary

Overall, the results of the RandomOverSampler LogisticRegression is better at predicting a High Risk Loan. The LogisticRegression is good at predicting the Healthy Loans since it had had so many more of those results and it seemed to overfit with that data. 
In this case, tring to correcly predict the High Risk Loans is more important than trying to predict the Healthy Loans.
I would recommend using the second model.
