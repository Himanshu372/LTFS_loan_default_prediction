# LTFS_loan_default_prediction
![title](ltfs.jpg)

# LTFS Data Science FinHack ( ML Hackathon)

## L&T Financial Services & Analytics Vidhya presents **‘DataScience FinHack’**.

In this FinHack, you will develop a model for our most common but real challenge **‘Loan Default Prediction’ & also, get a feel of our business!**

If your solution adds good value to our organization, take it from us, Sky is the limit for you!

## Problem Statement

### Vehicle Loan Default Prediction

Financial institutions incur significant losses due to the default of vehicle loans. This has led to the tightening up of vehicle loan underwriting and increased vehicle loan rejection rates. The need for a better credit risk scoring model is also raised by these institutions. This warrants a study to estimate the determinants of vehicle loan default.
A financial institution has hired you to accurately predict the probability of loanee/borrower defaulting on a vehicle loan in the first EMI (Equated Monthly Instalments) on the due date. Following Information regarding the loan and loanee are provided in the datasets:

* **Loanee Information (Demographic data like age, income, Identity proof etc.)**
* **Loan Information (Disbursal details, amount, EMI, loan to value ratio etc.)**
* **Bureau data & history (Bureau score, number of active accounts, the status of other loans, credit history etc.)**

Doing so will ensure that clients capable of repayment are not rejected and important determinants can be identified which can be further used for minimising the default rates.
 

### Data Description

* train.zip contains train.csv and data_dictionary.csv.
* train.csv contains the training data with details on loan as described in the last section
* data_dictionary.csv contains a brief description on each variable provided in the training and test set.
* test.csv contains details of all customers and loans for which the participants are to submit probability of default.
 


* sample_submission.csv contains the submission format for the predictions against the test set. A single csv needs to be submitted as a solution.
 

### Evaluation Metric

Submissions are evaluated on **area under the ROC curve** between the predicted probability and the observed target.
 

### Public and Private Split
Test data is further randomly divided into **Public (25%) and Private (75%)** data.
Your initial responses will be checked and scored on the Public data.
The final rankings would be based on your private score which will be published once the [competition](https://datahack.analyticsvidhya.com/contest/ltfs-datascience-finhack-an-online-hackathon/) is over.



### My approach 

Involved 4 steps
1. Preprocessing and Feature engineering - Preprocessing involved converting DOB and loan disbursal date into years and months from today respectively. Containerization of credit history scores and where the score wasn't available replacing those values by mean of the column. Using frequeny ratio for various features such as pincode, manufacture_id and employee_id. 

2. Model fitting - For baseline model, I started with Logistic Regression. Then I used Naive Bayes and XGBoost, after which I tried LGBM. LGBM didn't perform as expected. 

3. Model Optimization - For model optimization I used 3 fold validatioin. After using validation on all models created, I achieved max score for AUC metric on XGB of .576. I also tried using hyper parameter tuning for XGB, but training was taking too long.

 




 
