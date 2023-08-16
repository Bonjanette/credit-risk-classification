# credit-risk-classification

Module 20 Challenge CWRU Data Analytics Bootcamp

## Overview of the Analysis

The purpose of this analysis was to use supervised machine learning techniques to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was used to build two models that can identify the creditworthiness of borrowers. Peer-to-peer lending services have a higher loan default rate than typical banks, so it is important to develop a model that can predict those high risk loans so that investors can make more informed decisions about the risks they are accepting. The goal was to predict loan_status with "0" depicting healthy loans and "1" depicting high risk loans.</br>
First, the original data was split into training and testing sets using "train_test_split". A logistic regression model was fited to the training data set. Then predictions were generated using the testing data set. A balanced accuracy score, confusion matrix and classification report were generated to assess the effectiveness of the model.</br>
Second, RandomOverSampler was used to make predictions about this data set because the data set had relatively few "high risk" loan data entries. A random oversampler model was instantiated and the original training data was fit to the oversampler model. A Logistic Regression model was instantiated and fit to the resampled training data, and predictions were made. Balance accuracy score, confusion matrix, and a classification report were created using the oversample logistic regression model's results.

## Results

<ul>Logistic Regression using original data</br>
<li>Accuracy: 0.99</li>
<li>Precision for "healthy loans": 1.00</li>
<li>Precision for "high risk loans": 0.85</li> 
<li>Recall for "healthy loans": 0.99</li>
<li>Recall for "high risk loans": 0.91</li></ul>
<ul>Logistic Regression using oversampled data</br>
<li>Accuracy: 0.99</li>
<li>Precision for "healthy loans": 1.00</li>
<li>Precision for "high risk loans": 0.84</li> 
<li>Recall for "healthy loans": 0.99</li>
<li>Recall for "high risk loans": 0.99</li></ul>

## Summary

As indicated in the Recall results for the "high risk loans", the Oversampling model did a better job detecting the "high risk loans". It is important for investors to have an accurate assessment of higher risk loans so they can make sound decisions about their investments. Of the 2 models, the Oversampling model is better, however, 16% of the loans labeled by the Oversampling model as "high risk" were not actually "high risk", and this is problematic for those loans as they would likely be subject to higher rates unfairly. A model with higher precision for loans in the "high risk" category should be sought.
