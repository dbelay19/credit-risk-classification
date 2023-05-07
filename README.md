# Overview of credit-risk-classification analysis
_______________________________________________________________________________________________________________________________________________________________________
* The objective of this challenge is to help us apply what we have learned about machine learning and performing logistic analysis using various techniques by training and evaluating the model based on loan risk dataset of historical lending activity from a peer-to-peer lending services company.  I used this data to build a model that can identify the creditworthiness of borrowers. 
* To perform the analysis, I have set up all needed import functions, imported the lending_data.csv file from the resources file, read the data into a DataFrame, and setup dependent and independent variables. 
* The dependent variable (y value) in this analysis was the "loan status" indicating if a loan is healthy or a high-risk loan.
* The independent Variables (x values) were loan_size,	interest_rate,	borrower_income,	debt_to_income,	num_of_accounts,	derogatory_marks,	and total_debt.	
* Once the X and Y variables are set, I have splited the data into training and testing data stet and performed logistic regression using the original training data and saved the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.  After this, I evaluated the model’s performance by calculating accuracy score, confusion matrix and printing classification report.
* Moreover, I have performed prediction of  a logistic regression model with resampled training data. I used the RandomOverSampler module from the imbalanced-learn library to resample the data and ensured that the labels have an equal number of data points.
Performed similar analysis to the original data and compared model performance in predicting riskiness of a loan using the original and resampled data.


# Results
_______________________________________________________________________________________________________________________________________________________________________

* Results of logistic regression model with original data

![image](https://user-images.githubusercontent.com/117956888/236652592-86122da3-b8ac-4dc4-8a27-599f74dfa1a6.png)

* Logistic regression analysis results using the resampled data

![image](https://user-images.githubusercontent.com/117956888/236652642-d25fe187-cfb0-4443-aeac-9e12e9640caf.png)

# Credit Risk Analysis Report
_______________________________________________________________________________________________________________________________________________________________________
Based on the classification report, the logistic regression model fit with oversampled data has improved in predicting the minority class (label 1) compared to the model fit with original data, as seen by the higher recall and F1-score for label 1 (Risky loans). Moreover, the model's ability to predict the majority class (label 0) has also remained the same as original data which has a score of 1.0 (which is good) for precision, recall, and F1-score for label 0 (healthy loans). Overall, the accuracy score for the oversampled model is slightly higher than the original model. This suggests that oversampling can improve the model's ability to predict minority classes. This means that it is more effective at distinguishing high-risk loans with high recall and F1 score accuracy. It can be suggested also that the balanced data set of 1s and 0s in the resampled data might have helped to improve the model's accuracy in predicting loas that are classified as high risk in the original data set.
