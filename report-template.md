# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The purpose of this analysis is to evaluate logistic regression models developed to determine loan risk, and the effecitveness of those models.

* Explain what financial information the data was on, and what you needed to predict.

The financial information the data used to determine if a loan is healthy or not includes the loan size, the interest rate, the borrower's income, the debt to income ratio, the number of accounts the customer has, any derogatory marks on their credit and their total amount of debt. The goal is to use machine learning to look through these variables and predict the likelihood that the loan would be considered healthy or high risk for the financial institution.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The variables we are trying to predict are the loan status, and it was identified by using python's value_counts to see the total number of outcomes for the loan status. In this case a 0 indicated a healthy loan and a 1 indicated a high-risk loan.

* Describe the stages of the machine learning process you went through as part of this analysis.

The stages of the machine learning process included first importing the data and looking at the dataframe to see the different variables. Then I split the data into labels  and fatures for Y variable (i.e. loan status) and X variables (all of the other information provided). After that, it is imperative to split the data into training and testing variables in order to train the model and compare the training to the tested results. If selected the machine learning model, in this case a logistic regression, fit the model to tthe training data and predicted the data results. Then I compared the training data to the actual results using the balanced accuracy score, the confusion matrix and the classification report. Finally, I oversampled and resample the data and compared the outcomes of the two models.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

I used a logistic regression model because it is particularly good for classifying information, but can also be used for linear regressions as needed. Then for resampling, I imported the oversampler to add to the sample data and resample the data in order to compare the two logistic regression models. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
      *In Model 1, the overall balanced accuracy score was 95%. In this Healthy loans were identified with 100% precision and 99% recall and high-risk loans were identified with 85% accuracy and 91% recall.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
        *In Model 2, the overall balanced accuracy score was 99%. In this Healthy loans were identified with 100% precision and 99% recall and high-risk loans were identified with 84% accuracy and 99% recall.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
If you do not recommend any of the models, please justify your reasoning.

While the oversampled logistic regression had the best balanced accuracy score, I still would recommend use of the regular logistic regression model, as oversampling can lead to overfitting and model bias. Considering the accuracy score for high-risk loans was slightly lower with the oversampled data, I would still prefer to use Model 1. 

With that said, performance does depend on the problem you are trying to solve. It is obviously more important to accurately identify high-risk loans than healthy loans. If a loan is identified as high risk but ends up being healthy and not failing, then the bank still is able to collect interest on their loan and operate successfully. Conversely, the risk of a loan being misidentified as healthy, when it is in fact high-risk and ultimately fails, can lead to failed business outcomes for the financial institution. Therefore ensuring higher accuracy of identifying high risk loans is the most important data outcome. While oversampling can be beneficial to increase representation for a minority class in a dataset, in this particular instance, I do not recommend utilizing that sample.
