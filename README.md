# Module 12 Assignment - Supervised Machine Learning

## Overview of the Analysis

The purpose of this analysis is to be able to predict the creditworthiness of new borrowers. The data used is from a peer-to-peer lending services company that that has the details of a borrower for each loan. Some of the details in this dataset include borrower's income and the interest rate of the loan. The data we were trying to predict was the loan status column which contained `0's` for a healthy loan and `1's` for loans with a high risk.

I made 2 trained for this assignment, using the same machine learning model which was `Logistic Regression`. For the second model, I used the `RandomOverSampler` module to do a resample by balancing out the count for healthy and risky loans. To make the models I did the following steps:

1. I did a `train_test_split` on the data where 75% of it becomes the training data. y labels are the loan status while X are all the other features.
2. I created a model framework by **instantiating** the `LogisticRegression` module.
3. I then **trained** the model with the test data created from step 1.
4. After the training, I made the model **predict** the `loan_status` of the test data from step 1 (which would be the remaining unused 25%).
5. The ending of the analysis was to **evaluate** the success of the predictions by checking the `balanced_accuracy score`, `confusion_matrix`, and `classification_report`.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

After R

* Logistic Regression model with original data:
  * Balanced Accuracy: 0.9520
  * Precision (Healthy Loans): 1.00
  * Precision (Risky Loans): 0.85
  * Recall (Healthy Loans): 0.99
  * Recall (Risky Loans): 0.91



* Logistic Regression model with resample data:
  * Balanced Accuracy: 0.9937
  * Precision (Healthy Loans): 1.00
  * Precision (Risky Loans): 0.84
  * Recall (Healthy Loans): 0.99
  * Recall (Risky Loans): 0.99

## Summary

Both models seem to be similar and the key here is the difference in Risky loans metrics since that is the purpose of this study. In precision, there is a 0.1 difference that gives the advantage to the original model. The resample on the other hand has 0.08 higher recall for risky loans than the original model. Given also that the balanced accuracy for the resample model is higher by 0.0417, I would like to say that the second model is the better and the more preferred to predict risky loans. 
