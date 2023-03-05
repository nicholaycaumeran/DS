# Data Science Portfolio

# BG/NBD and Gamma/Gamma Model
## Model Description
BG/NBD Beta-Geometric/Negative-Binomial Distribution and Gamma-Gamma Models

These models are used in Customer Lifetime Value (CLV) analysis to estimate the expected value of a customer to a business over the course of their relationship.
The BG/NBD model is a probabilistic model that can be used to predict the number of future purchases a consumer is likely to make based on their past purchase history.
The Gamma-Gamma model is another probabilistic model used to estimate the monetary value of a user's future purchase based on their past contribution history.

## Variable Definitions
* Frequency - count of repeat purchases/contributions
* Recency - duration between a customer’s first contribution/purchase and latest one
* Time (T) - age of a customer within the chosen time unit. This is equal to the duration between a customer’s first contribution/purchase and the end of the period under study
* Monetary Value - the value of each purchase/contribution 

## Model Output
BG/NBD model predicts:
* the number of purchases one will make in k future periods
* the probability of one being active at the end of the observation period

Gamma-gamma model predicts:
* the average transaction value & lifetime value (LTV) of customer over the set period and set monthly discount rate

## Practical Insights and Usage
* Target customers based on Churn Rate/P(Alive) - Segment customers based on probability of being alive to Churned, Not Churned, High Risk of Churn and develop startegies to target to reactive or retain them to encourage loyalty. 
* Profile High-Value Customers and target customers having similar profiles to acquire customers

## Model Limitations
* Based on the paper on BG/NBD model ("Counting Your Customers" the Easy Way, "the BG/NBD model forecasts tend to be relatively poor when penetration and/or purchase frequency are extremely low. In a world where active buyers are either uncommon or very slow in making their purchases, BG/NBD will be outperformed by the Pareto/NBD model. In this case, the one-time buyers (20% of customers) were removed before fitting the models. Pareto/NBD model should be fitted and compared. 





