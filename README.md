# Customer Churn Prediction Using Machine Learning

## Overview

This project analyzes customer churn behavior (whether a customer will leave or stay)and builds a machine learning model to predict churn using historical customer data.

The goal is to help businesses identify customers at risk of leaving so
they can take proactive retention actions.

The project is built using Python and scikit-learn.

------------------------------------------------------------------------

## Problem Statement

Customer churn is a major issue for subscription-based businesses.
Losing customers directly affects revenue and growth.

This project aims to: - Predict if a customer will churn - Understand
key factors influencing churn - Provide insights for customer retention
strategies

------------------------------------------------------------------------

## Dataset

The dataset contains customer information such as: - Contract type -
Monthly charges - Tenure - Internet service - Payment method - Churn
status (Yes/No)

Source: - Kaggle Telco Customer Churn Dataset

------------------------------------------------------------------------

## Tools & Technologies

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Scikit-learn

------------------------------------------------------------------------

## Project Workflow

### 1. Data Cleaning

-   Removed unnecessary columns (e.g. customerID)
-   Handled missing values
-   Converted target variable into numerical format

### 2. Exploratory Data Analysis (EDA)

-   Analyzed churn distribution
-   Compared churn across contract types
-   Studied relationship between churn and monthly charges
-   Identified patterns in customer tenure

### 3. Data Preprocessing

-   Converted categorical variables using one-hot encoding
-   Split dataset into features (X) and target (y)

### 4. Model Building

-   Split data into training and testing sets
-   Trained Logistic Regression model using scikit-learn

### 5. Model Evaluation

-   Evaluated using:
    -   Accuracy score
    -   Classification report
    -   Confusion matrix

------------------------------------------------------------------------

## Machine Learning Model

-   Logistic Regression (Binary Classification)

------------------------------------------------------------------------

## Results

The model successfully predicts customer churn with reasonable accuracy and provides meaningful insights into customer behavior.

It helps identify high-risk customers and supports business decision-making for customer retention.

------------------------------------------------------------------------

## Key Insights

-   Month-to-month customers are more likely to churn
-   Higher monthly charges increase churn probability
-   Longer tenure reduces churn risk

------------------------------------------------------------------------

## Recommendations

- Offer discounts for month-to-month customers
- Improve onboarding experience for new customers
- Encourage long-term contracts with incentives

------------------------------------------------------------------------

## Author

Muktar Bello

