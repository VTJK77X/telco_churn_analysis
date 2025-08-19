# Telco Customer Churn Analysis
## Project Overview
This project performs an in-depth analysis of a fictional telecommunications company's customer churn data. The primary goal is to identify the key factors that contribute to customers discontinuing their services. By understanding these drivers, the company can develop targeted strategies to improve customer retention.

The analysis leverages SQL queries directly on a pandas DataFrame using the duckdb library for efficient data manipulation and aggregation. The notebook explores various aspects of the customer data, including demographics, subscribed services, and financial information, to uncover patterns related to churn.

## Key Questions Addressed
- What is the overall customer churn rate?
- How do demographic factors like gender, age (senior citizens), and family status (partners, dependents) influence churn?
- Which services are most or least associated with customer churn?
- What is the relationship between contract type, payment method, tenure, and a customer's likelihood to churn?
- What are the most significant predictors of churn based on their Information Value (IV)?

## Dataset
The analysis uses the "Telco Customer Churn" dataset, which contains information about 7,043 customers and includes the following details:
Customer Demographics: gender, SeniorCitizen, Partner, Dependents.
Services Subscribed: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies.
Account Information: tenure, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges.
Target Variable: Churn (Yes/No).

## Methodology
The analysis was conducted within a Jupyter Notebook.
Data Loading and Cleaning.
The dataset is loaded into a pandas DataFrame.
Data types are corrected (e.g., TotalCharges to numeric, categorical columns to category type for memory efficiency).
The SeniorCitizen column is mapped from 0/1 to a more descriptive 'No'/'Yes'.
A small number of rows with missing TotalCharges are dropped.

## Exploratory Data Analysis (EDA)
The skimpy library is used for a comprehensive statistical summary of the dataset.
The duckdb library is employed to run complex SQL queries for segmenting the data and calculating churn rates across various customer attributes. This approach allows for powerful and readable data aggregation.

## Feature Importance Analysis
Information Value (IV) and Weight of Evidence (WoE) are calculated for all categorical variables to measure their predictive power in relation to the churn outcome. This helps quantify which factors are most significant.
