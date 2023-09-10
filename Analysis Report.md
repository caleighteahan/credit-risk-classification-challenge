# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to evaluate machine learning models and to decide which one is most effective at accurately making predictions for the data provide. 
* Explain what financial information the data was on, and what you needed to predict. The data provided was based on individuals loans and wether they were in good or bad standing, as well as contextual values such as interest rate and borrower's income. This helps our model get a better idea of the loan and the borrower so it could better predict the status of a loan beign healthy or not. To predict this we used the column of "loan_status" in the source data which was set as variable y. From there we can see how many loans are healthy or not (via value_counts). We then set the rest of the data to the variable X, which includes a multitude of factors (ie. loan size, total debt, deragatory marks, etc. ). We took these two variable, split them into training and testing sets, and then used Linear Regressiona and RandomOverSampler to create our models 


## Results

* Machine Learning Model 1:
Below we can see the scores for Model 1:
  
  precision    recall  f1-score   support

            0       1.00      0.99      1.00     18765
            1       0.85      0.91      0.88       619

      accuracy                           0.99     19384
    macro avg       0.92      0.95      0.94     19384
  weighted avg       0.99      0.99      0.99     19384

The linear regression model, model 1, yield high accuracy, precision and recall score both in general and for prediction loans with the label 0. It was less successful with loans labeled 1 but the scores for it are in general good scores.



* Machine Learning Model 2:
Below are the scores for Model 2:
    precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384

The RandomOverSampler model. model 2, also yielded high results for the data. Like linear regression it was less successful with predicting loans labeled with a 1, but generated high results than model 1.

## Summary

In conclusion, model 2 was proven the better model for prediction based on the higher accuracy scores it yielded. Especially since it was, in general, better at predicting loan labeled with a 1 as opposed to model 1. This is important because a 1 labels mean the loan is unhealthy and these are the type of loan we want our machine to catch to identify the creditworthiness of borrowers.
