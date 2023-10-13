# Loan Eligibility Predictive Analytics with R

## Problem Statement

The Loan Prediction project is aimed at automating the loan eligibility assessment process for a finance company. The company receives online loan applications with various customer details, and they want to identify the eligible customers in real-time. This project uses Machine Learning to predict whether a customer's loan application should be approved or not.

## About the Company

The company, Dream Housing Finance, operates in urban, semi-urban, and rural areas, offering home loans. To streamline their loan eligibility process, they seek to automate it based on customer details provided during the online application.

## Data

The data used in this project includes various customer attributes such as Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History, and more. This dataset is a crucial component for predicting loan eligibility.

### Credit Risk Indicators

In this project, we considered various credit risk indicators to build the predictive model. Some of the key credit risk indicators included:

1. **Credit History**: Applicants with a good credit history are more likely to be eligible for loans.

2. **Loan Amount**: The amount requested by the applicant can indicate their financial stability and ability to repay the loan.

3. **Income**: Higher income applicants are generally more favorable for loan approval.

4. **Education**: Education level can also be a factor. Graduates may have better chances of loan approval.

5. **Property Area**: The area in which the property is located may influence loan eligibility.

6. **Self-Employment**: Self-employed individuals may have different eligibility criteria compared to salaried individuals.




## Checking the Data

To ensure data quality, the project checks for anomalies and missing values in the dataset. Data errors and missing data are identified and handled as part of the preprocessing phase. This step includes understanding the data distribution, handling missing values, and making data corrections.

## Tidying the Data

To prepare the data for modeling, various data preprocessing steps are performed. Missing values are imputed using the Multiple Imputation by Chained Equations (MICE) method. Outliers are treated using log transformations for Loan Amount and Applicant Income. Additionally, a new variable, Total Income, is created by combining Applicant Income and Co-applicant Income.

## Statistical Analysis

We conducted a thorough statistical analysis of the dataset to gain insights and identify patterns. This analysis included:

- Data exploration to understand the distribution and characteristics of the variables.
- Treatment of missing data and outliers to ensure data quality.
- Visualization of data through histograms, box plots, and bar charts to identify trends and patterns.
- Handling of categorical variables and data transformation to improve model performance.

## Building Predictive Models

### Logistic Regression

The project starts by building a Logistic Regression model. The model initially uses Credit History as the only predictor variable. Subsequently, additional variables like Education, Self-Employed, Property Area, Loan Amount, and Income are included to improve accuracy. The model is trained and evaluated on both training and test datasets.

### Decision Tree

A Decision Tree model is constructed to classify loan applications. The decision tree is grown, pruned, and visualized. The model is evaluated on both the training and test datasets to assess its accuracy.

### XGBoost 
we chose to use the XGBoost algorithm to build our predictive model. XGBoost is known for its superior performance in various machine learning tasks, including classification. It can handle large datasets, provides excellent predictive accuracy, and helps prevent overfitting

## Chosen Model & Scoring

The XGBoost model is selected for its competitive accuracy and robustness. This model offers a good balance between training and testing performance. It is capable of handling new data with similar predictor variables for loan eligibility prediction.

## Generating Predictions

The chosen XGBoost model is applied to a test dataset to make predictions about loan eligibility. These predictions are stored in a CSV file, which contains Loan_ID and Loan_Status columns. This file can be used to identify eligible customers in real-time applications.

## Conclusion

The Loan Prediction project demonstrates the use of machine learning algorithms to automate the loan eligibility assessment process. By analyzing customer attributes, the model accurately predicts whether a loan application should be approved. The Random Forest model is selected for its strong performance, and the project generates predictions for new loan applications.











