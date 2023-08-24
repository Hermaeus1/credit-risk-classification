# Module 20 Challenge Report

## Overview of the Analysis

In this challenge, the goal of this analysis is to create models that can identify high-risk loans with decently high accuracy.
These models were generated with features such as loan amount, the borrower's income, the incumbent debt-to-income ratio, number of open accounts, number of derogatory marks (like missed or late payment), and their total debt. All these features were used to predict whether or not a particular loan is in good standing, or at a high risk of default. For both models, we first had to split our data into a set to train on and a set to test with. This includes splitting off the aforementioned features into their own data frame as to not train with the loan status included. After that, each model used a form of logistic regression to predict which loans are high-risk. Additionally, the second model was done with an oversampled data to train on equal parts high risk to low risk loans. Once both models were completed, their accuracy was checked to both having a precision of 87% and the oversampled model to have a better recall rate for high-risk loans. This makes sense as oversampling strongly weights high-risk loans in the learning algorithm and fills the training data with repeats. This makes the model more sensitive to high-risk loans, but may also affect real world performance.

## Results

* Machine Learning Model 1 (Standard Logistic Regression):
  * Balanced Accuracy: 94.4%
  * Precision: Healthy; 100%, High-Risk 87%
  * Recall: Healthy; 100%, High-Risk 89%



* Machine Learning Model 2 (Oversampled Logistic Regression):
  * Balanced Accuracy: 99.5%
  * Precision: Healthy; 100%, High-Risk 87%
  * Recall: Healthy; 100%, High-Risk 100%

## Summary

    *The OverSampled model seems to perform better as its balanced accuracy is higher by 5.1%. However, this model will be more susceptible to bias from over sampling the high-risk loan data.
    *If we are trying to model who will have good loans, performance is not as needed since their is an abundance of healthy loans present in our data. In the case of identifying high-risk loans, high-performance is crucial as to not give out loans that will likely default and not deny those who would otherwise have healthy loans (missed revenue).
    Overall for identifying risky loans, I would recommend the OverSampled logistic regression model with the caveat that all loans should be continuously audited for their loan standing and the training data updated accordingly. It is also extremely important to continually feed in new data as it becomes available due to inflation of incomes and the higher variability in interest rates. If any general pre-approval modeling wants to be done, the first model will suffice as it requires less data, and is more balanced towards the usual "good-credit joe".

