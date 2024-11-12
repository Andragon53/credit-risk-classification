# Module 12 Report

## Overview of the Analysis

The purpose of this analysis is to determine the viability of training and utilizing a supervised machine learning model to evaluate a peer-to-peer lending service's activity for loan risks, and a borrower's creditworthiness. The model that will be tested is a Logistic Regression model, with will be trained to evaluate a given loan's application data, taking features into account such as the loan amount and interest, the borrower's accrued debt and income, and any derogatory marks against the borrower, and then make a decision on whether the loan's "loan_status" variable is either 0 (a healthy loan) or a 1 (high-risk loan). The historical loan report data that was provided as part of the analysis was split up unevenly; one into a larger "training set" that the model used to create it's calculated model of both healthy and high-risk loans, and the other into a "testing set" that would be used to evaluate the model's accuracy and precision of it's predictions of all future data inputs.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression
    * Accuracy: 99% accuracy indicates that the model as a whole will return very few false results, which is a high mark in the model's favor.
    * Precision: The reports show that the model correctly labelled 99.9% of the test data's healthy loan items, but only 84% of the high-risk loans, meaning a number of false positives were identified in the model's data predictions.
    * Recall: The reports show that the model correctly labelled 99% of the test data's healthy loan items an 94% of the high-risk loans, meaning a few false negatives were identified in the model's data predictions.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The Logistic Regression model has very high accuracy, meaning false predictions are going to happen few and far between. Of the false predictions, false positives on loan_status "1" were the most common, which would cause trouble if perfectly normal loans were incorrectly marked as high-risk. The rest of the model's evaluation statistics are high enough to show that the model performs at a high level of accuracy and precision otherwise. Overall, I would recommend the Logistic Regression machine learning model as the model to run the lending service's risk-detection software, but with a caveat that there is still a human operator reviewing the algorithm's predictions, in order to catch false positives that could lead to borrowers being incorrectly flagged for credit score reductions.