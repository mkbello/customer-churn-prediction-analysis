# Customer Churn Prediction and Analysis

## 1. Project Overview

Customer churn occurs when customers stop using a company's products or services. Retaining existing customers is important because losing customers can negatively affect business revenue and growth.

This project applies machine learning to predict customer churn in a telecommunications company. The goal is to identify customers who are likely to leave, understand the factors associated with churn, and provide insights that support better customer-retention strategies.

The project combines machine learning, data analysis, and business intelligence using Python and Power BI.

## 2. Project Objectives

- Explore and understand customer data.
- Clean and prepare the dataset for machine learning.
- Perform exploratory data analysis to identify patterns and trends.
- Build and evaluate different classification models.
- Identify the model that best detects potential churners.
- Interpret important features associated with customer churn.
- Provide practical business recommendations based on the findings.
- Develop an interactive Power BI dashboard to communicate key business insights.

## 3. Dataset Description

The project uses the publicly available Telco Customer Churn dataset.

- **Total Records:** 7,043
- **Original Features:** 19
- **Target Variable:** `Churn`
- **0:** Customer did not churn.
- **1:** Customer churned.

The dataset contains information about customer demographics, account details, subscribed services, contract types, and payment methods.

## 4. Project Workflow

The project followed these major steps:

1. **Data Exploration:** Examined the dataset structure, data types, distributions, and relationships between variables.
2. **Data Cleaning:** Checked and handled missing values, corrected data types, and prepared the dataset for analysis.
3. **Exploratory Data Analysis:** Examined customer characteristics and identified patterns associated with churn.
4. **Data Preprocessing:** Encoded categorical variables and scaled numerical features.
5. **Train-Test Split:** Divided the dataset into training and testing sets using an 80:20 split.
6. **Model Building:** Trained four classification algorithms.
7. **Model Evaluation:** Compared model performance using accuracy, precision, recall, F1-score, and confusion matrices.
8. **Hyperparameter Tuning:** Used GridSearchCV to optimise Logistic Regression.
9. **Model Interpretation:** Examined model coefficients, individual predictions, prediction outcomes, and high-risk customers.
10. **Business Recommendations:** Developed recommendations based on the model findings.
11. **Dashboard Development:** Built an interactive Power BI dashboard to present customer churn metrics and business insights.

## 5. Machine Learning Models

The following classification algorithms were evaluated:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Artificial Neural Network (ANN)

## 6. Model Performance

The initial model comparison produced the following results:

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 80.62% | 65.93% | 55.88% | 60.49% |
| KNN | 76.30% | 55.38% | 55.08% | 55.23% |
| SVM | 79.49% | 65.45% | 48.13% | 55.47% |
| ANN | 76.93% | 57.36% | 51.07% | 54.03% |

Logistic Regression achieved the best initial overall performance and was selected for further optimisation.

### Optimised Logistic Regression

GridSearchCV was used to optimise the Logistic Regression model.

| Metric | Score |
|---|---:|
| Accuracy | 74.31% |
| Churn Precision | 51.05% |
| Churn Recall | 78.34% |
| Churn F1-Score | 61.81% |

The optimised model achieved higher recall and F1-score for the churn class compared with the original Logistic Regression model.

Although its accuracy and precision decreased, it identified a larger proportion of actual churners.

## 7. Selected Model

The optimised Logistic Regression model was selected as the final model because identifying potential churners is a major objective of this project.

Its churn recall of 78.34% means that it correctly identified approximately 78 out of every 100 actual churners in the test set.

However, the model also produced false-positive predictions. Therefore, its predictions should be treated as indicators for further customer-retention assessment rather than guaranteed outcomes.

## 8. Model Interpretation and Key Findings

Model interpretation was performed using Logistic Regression coefficients and individual customer predictions.

The analysis highlighted several features associated with customer churn:

- **Contract Type:** Customers with two-year contracts showed a lower model association with churn.
- **Tenure:** Longer customer tenure was associated with a lower likelihood of churn.
- **Fiber Optic Internet:** This feature showed a positive association with churn predictions.
- **Electronic Check:** Customers using electronic check payments showed a higher model association with churn.
- **Online Security and Tech Support:** Having these services was associated with a lower likelihood of churn.
- **Paperless Billing:** This feature showed a positive association with churn predictions.

The individual prediction analysis also identified customers with high estimated churn probabilities.

These findings describe patterns identified by the model. They do not establish that the features directly cause customers to churn.

## 9. Business Recommendations

Based on the project findings, the following recommendations are proposed:

1. **Encourage Long-Term Contracts:** Offer suitable incentives and loyalty benefits to encourage customers to consider longer-term contracts.
2. **Prioritise High-Risk Customers:** Identify customers with high predicted churn probabilities and prioritise them for retention campaigns.
3. **Improve Technical Support:** Improve the quality and accessibility of technical support services.
4. **Review Fiber Optic Services:** Investigate customer satisfaction, service quality, and pricing associated with fiber optic internet.
5. **Improve Payment Experience:** Investigate payment-related concerns and make payment processes more convenient.
6. **Monitor Customer Churn:** Regularly analyse customer behaviour and use predictive insights to support retention decisions.

## 10. Power BI Dashboard

An interactive Power BI dashboard was developed to present the key findings of the customer churn analysis.

**Dashboard Name:** Churn Analysis Overview

### Key Performance Indicators (KPIs)

- Total Customers
- Churned Customers
- Retained Customers
- Overall Churn Rate

### Dashboard Visualisations

- Churned Customers by Contract Type
- Churn Rate by Tenure Group
- Churn Rate by Internet Service
- Churn Rate by Payment Method

### Interactive Slicers

- Gender
- Contract
- Internet Service

### Key Dashboard Insights

- Month-to-month customers account for the highest number of churn cases.
- Churn varies across customer tenure groups.
- Fiber optic customers have the highest churn rate (41%), compared with DSL customers (18%) and customers without internet service (7%).

The dashboard provides an interactive and business-focused view of customer churn patterns, allowing users to explore customer segments and identify areas requiring retention attention.

## 11. Tools and Technologies

- **Python:** Programming language
- **Pandas:** Data manipulation and analysis
- **NumPy:** Numerical computing
- **Matplotlib:** Data visualisation
- **Seaborn:** Statistical data visualisation
- **Scikit-learn:** Machine learning and model evaluation
- **Joblib:** Saving and loading trained models and preprocessing objects
- **Jupyter Notebook:** Data analysis and model development
- **Power BI:** Interactive dashboard development
- **Git and GitHub:** Version control and project hosting

## 12. Project Structure

```text
Customer_Churn/
│
├── dashboard/
│   └── Customer_Churn_Analysis_Dashboard.pbix
|
├── data/
│   ├── raw/
│   │   └── customer_churn.csv
│   │
│   └── processed/
│       ├── cleaned_customer_churn.csv
│       ├── prepared_data.pkl
│       └── standard_scaler.pkl
│
├── models/
│   └── best_churn_model.pkl
│
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Exploratory_Data_Analysis.ipynb
│   ├── 03_Data_Preprocessing.ipynb
│   ├── 04_Model_Building_Evaluation.ipynb
│   └── 05_Model_Interpretation.ipynb
│
├── visualizations/
|   ├── churn_by_contract.png
│   ├── churn_distribution.png
│   ├── confusion_matrix.png
│   ├── feature_importance_chart.png
|   ├── tenure_distribution.png
│   └── model_performance_comparison.png
│
└── README.md
```

## 13. Conclusion

This project demonstrates how machine learning and business intelligence can be applied to customer churn prediction and analysis.

Four classification algorithms were evaluated, and Logistic Regression was further optimised using GridSearchCV. The final model achieved a churn recall of 78.34%, providing a useful approach for identifying customers who may be at risk of leaving.

Model interpretation revealed important customer characteristics associated with churn, providing a basis for practical retention recommendations.

An interactive Power BI dashboard was also developed to communicate the project's key performance indicators, customer churn patterns, and business insights.

Overall, the project demonstrates how predictive modelling and data visualisation can support more informed customer-retention decisions in the telecommunications industry.
