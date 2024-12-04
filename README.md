# Introduction

This churn_rate_analysis notebook investigates customer churn for a beverage subscription service. The goal is to develop a machine learning model to predict customer churn and implement targeted retention strategies to minimize cancellations and ensure business sustainability.

# Data Exploration
The analysis delves into historical customer data, focusing on key variables such as:

Customer Demographics:
- Age
- Gender
- Employment Status

Subscription Details:
- Subscription Start Date
- Subscription End Date
- Monthly Payment Amount
- Total Payments
- Cancellation Reason
- Last Order Date
- Total Subscriptions
- Payment Method

# Key Findings
- High Churn Rate: A significant 24.1% of customers have canceled their subscriptions.
Primary Reasons for Cancellation:
- Customer Dissatisfaction (32.6%)
- Desire for Alternative Service Providers (35.4%)
- Gender Disparity: Female customers exhibit a slightly higher churn rate.
- Employment Status Impact: Employed customers have a higher churn rate compared to unemployed and student customers.
- Payment and Age Factors: Customers with higher monthly payments and older customers tend to have higher churn rates.

# Data Visualization
Visualizations like countplots and density plots were used to explore the distribution of variables across different subscription statuses (active/cancelled). This helped identify patterns and potential relationships between customer characteristics and churn.

# Statistical Analysis
Correlation analysis was performed to assess the relationship between variables. However, the p-values for several variables (monthly payment amount, age, total subscriptions, total payments) were greater than 0.05, indicating a lack of statistical significance.

# Predictive Modeling
Machine learning models, including Random Forest and Support Vector Machines, were trained on the historical data to predict customer churn. These models prioritized high recall to effectively identify customers at risk of canceling.

Predicting Churn for New Customers
The Random Forest model predicted an 8.2% churn rate for new customers. This insight can be used to proactively implement retention strategies and minimize future churn.

# Conclusion
This churn rate analysis provides valuable insights into customer behavior and the factors influencing cancellations. By addressing customer dissatisfaction, improving service quality, and implementing targeted retention strategies, the beverage subscription service can significantly reduce churn and enhance customer loyalty.















