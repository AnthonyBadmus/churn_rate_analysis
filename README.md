# Introduction

This churn_rate_analysis notebook investigates customer churn for a beverage subscription service. The goal is to develop a machine learning model to predict customer churn and implement targeted retention strategies to minimize cancellations and ensure business sustainability.

# Data Description

The data includes customer information such as:

customer_id (object)
subscription_start_date (object)
subscription_end_date (object)
subscription_status (object) - Active or Cancelled
monthly_payment_amount (float64)
total_payments (int64)
cancellation_reason (object)
last_order_date (object)
age (int64)
gender (object)
employment_status (object)
total_subscriptions (int64)
payment_method (object)
The data is assumed to be generated using Faker.

# Exploratory Data Analysis (EDA)

The EDA phase involves:

Checking Data
(Overview) - Provides information about rows, columns, data types, and null values.
(Number of Classes) - Displays the number of unique categories for categorical variables.

Descriptive Statistics - Summarizes numerical variables using mean, standard deviation, etc.
Visualizing Categorical Variables

Count plots are used to visualize the distribution of subscription status, cancellation reasons, subscription status by gender, and subscription status by employment status.
Visualizing Numeric Variables

Distribution plots are created to compare the distribution of monthly payment amount, age, and total subscriptions between active and cancelled subscriptions.
Correlation heatmap is generated to explore relationships between numerical variables.
Checking for Relationship Between Variables

Correlation coefficients and p-values are calculated to assess the strength and significance of relationships between numerical variables and the target variable (subscription status).
# Data Preprocessing

Feature Engineering

last_order_date and subscription_start_date are converted to datetime format.
recency is calculated as the difference (in days) between the current date and the last order date.
tenure is calculated as the difference (in days) between the current date and the subscription start date.
Encoding Categorical Variables

Label encoding is applied to convert categorical string variables (payment_method, gender, employment_status, and subscription_status) into numerical representations.
Training a Model

Feature Selection

The script currently includes all features for model training. You can modify this section to select relevant features based on feature importance or other techniques.
Model Training and Evaluation

The following machine learning models are trained and evaluated:
Logistic Regression
Random Forest Classifier
Support Vector Machine (SVM)
Performance metrics include accuracy, precision, recall, F1-score, and confusion matrix for each model.
Predicting Customer Churn

# Data Preparation for New Customers

New customer data is preprocessed similarly to the original data, including feature engineering and encoding categorical variables.
Model Selection

The Random Forest Classifier model is chosen for prediction due to its high recall (100%).
Prediction

The chosen model predicts the subscription status (active or cancelled) for the new customer data.
Analysis of Predictions

The predicted churn rate for new customers is calculated and presented.

# Findings and Conclusion

The analysis reveals key insights into customer churn, including:

High overall churn rate (24.1%)
Customer dissatisfaction and preference for alternative providers as leading reasons for cancellation
Gender disparity, employment status impact, monthly payment influence, and age-related patterns in churn
No statistically significant relationships found between some numerical variables and subscription status (may require further investigation or model refinement)
The Random Forest Classifier model predicts an 8.2% churn rate for new customers.

# Recommendations

Based on the findings, the following recommendations are made:

Address customer dissatisfaction and improve service quality.
Develop targeted retention strategies for different customer segments (gender, employment status, etc.).
Analyze pricing strategy and perceived value for customers.
Consider further investigation into factors influencing churn, potentially refining the model for better prediction accuracy.
By implementing these recommendations, the beverage subscription service can effectively reduce churn, enhance customer loyalty, and achieve long-term success.
