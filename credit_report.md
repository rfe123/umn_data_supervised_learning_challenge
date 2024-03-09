# Module 12 Report Template

## Overview of the Analysis

In this challenge, we leverage supervised machine learning to build a model for prediction of credit-worthiness for loan applicants. Our aim is to predict whether an applicant will default on the loan provided. 

We apply a Logistic Regression model to a lending data set provided in csv. For this exercise, a positive `1` results indicates a default prediction on the loan.

## Results

Overall, our Logistic Regression model provides a predicition accuracy of `99%` compared against the test data extracted from our original dataset.

* Logstic Regression Model:
  * Confusion Matrix
  
    |          |   Predicted 0 |   Predicted 1 |
    |:---------|--------------:|--------------:|
    | Actual 0 |         18679 |            80 |
    | Actual 1 |            67 |           558 |

  * For the sample data, we provide `19384` records. Of these, `147` results incorrectly predict the output, with `80` false positives.
  * We also observe `67` false negatives - where the model incorrectly predicts a 0.

## Summary

Our classification report from the challenge (shown below) indicates an overall accuracy of the model of 99%.

Classification Report

              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

    accuracy                           0.99     19384
    macro avg       0.94      0.94     0.94     19384
    weighted avg    0.99      0.99     0.99     19384

That said, referring back to the Confusion Matrix, we observe a larger percentage of incorrect predictions when the model predicts a loan default, with `12%` of the results being false positives. 

For that reason, I recommend using this model as a first step in our loan screening process, with further investigation required where the model indicates a likely default.