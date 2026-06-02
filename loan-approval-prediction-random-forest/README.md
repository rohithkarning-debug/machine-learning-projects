# Loan Approval Prediction using Random Forest Classification

## Overview
This project uses Random Forest Classification to predict whether a loan application will be approved based on applicant information such as income, education, employment status, loan amount, credit history, and property area.

## Dataset Information
- Records: 614
- Features: 11 predictor variables
- Target Variable: Loan_Status

### Target
- Y = Approved
- N = Rejected

### Features
- Gender
- Married
- Dependents
- Education
- Self_Employed
- ApplicantIncome
- CoapplicantIncome
- LoanAmount
- Loan_Amount_Term
- Credit_History
- Property_Area

## Why Random Forest?
- Ensemble learning algorithm
- Reduces overfitting
- Handles mixed feature types
- Strong performance on tabular data
- Provides feature importance analysis

## Preprocessing
1. Removed Loan_ID
2. Encoded categorical variables
3. Train-test split
4. Random Forest training

## Model
Random Forest Classifier

Parameters:
- Criterion = Entropy
- Random State = 0

## Results

Accuracy: 80.52%

Confusion Matrix:

[[24, 19],
 [11, 100]]

## Evaluation Metrics
- Accuracy Score
- Confusion Matrix
- Classification Report

## Visualizations
- Confusion Matrix
- Loan Approval Distribution
- Feature Importance Plot
- Accuracy Plot

## Conclusion
The Random Forest classifier achieved an accuracy of 80.52% on the loan approval dataset and demonstrates the effectiveness of ensemble learning techniques for financial classification problems.
