## Module 20 Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  - The purpose of this analysis is to determine if logistic regression can accurately predict healthy loans versus high-risk loans using the original dataset or a dataset that is resampled to increase the size of the minority class.
* Explain what financial information the data was on, and what you needed to predict.
  - The dataset used to preform the analysis consists of information on 77,536 loans. The columns for this dataset are as follow: loan_size, interest_rate, borrower_income, debt_to_income ratio, number of accounts, derotatory_marks, total_debt, and loan_status. The category that I am attempting to predict with this analysis is 'loan_status', all other columns will be used as features to train the the model and make predictions.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  - The columns for this dataset are as follow: loan_size, interest_rate, borrower_income, debt_to_income ratio, number of accounts, derotatory_marks, total_debt, and loan_status. The category that I am attempting to predict with this analysis is 'loan_status', all other columns will be used as features to train the the model and make predictions.
* Describe the stages of the machine learning process you went through as part of this analysis.
  - The stages are as follow:
    Prepare the Data -- import the file and create and evaluate the dataframe.
  - Separate the data into features and labels -- the labels that I am wanting to predict is the status of the loan healthy (0) or high-risk (1). The features are all of the remaining data used to train the model.
  - Use train_test_split function to separate the features and labels data into training and testing datasets.
  - Import the machine learning model from the scikit-learn library to fit, train, predict, and evaluate the predictions. Evaluations such as accuracy score, confusion matrix, and classification report.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
  - Primary model = LogisticRegression model from scikit-learn.
  - Supporting functions: train_test_split
  - Models evaluated by: confusion_matrix and classification_report (both from scikit-learn)

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model - LogisticRegression:
    * Accuracy Score: 99%
    * Precision Score:
        Class 0 (Healthy Loans): 100%
        Class 1 (High-Risk Loans): 85%
    * Recall Scores:
        Class 0 (Healthy Loans): 99%
        Class 1 (High-Risk Loans): 91%

## Summary

The model does a great job at predicting the values of the healthly loans--precision was 100% and the recall was 99%.

The model is also does a good job of predicting the values of high-risk loans, but not as good as predicting the healthy loans--precision was 85% and the recall was 91%.

Given this information, it appears the the logistic regression model does a great job at predicting both healthy and high-risk loans, given the features used to train the data.
