# BG/NBD and Gamma/Gamma Model

## Model Description
BG/NBD Beta-Geometric/Negative-Binomial Distribution and Gamma-Gamma Models are used in Customer Lifetime Value (CLV) analysis to estimate the expected value of a customer to a business over the course of their relationship.

* The BG/NBD model is a probabilistic model that can be used to predict the number of future purchases a consumer is likely to make based on their past purchase history.
* The Gamma-Gamma model is another probabilistic model used to estimate the monetary value of a user's future purchase based on their past contribution history.


## Data Information
Data was taken from UCI Machine Learning Repository, which contains transnational data set with all the transactions occurring between 01/12/2010 and 09/12/2011 for UK-based and registered non-store online retail. The company primarily sells unique all-occasion gifts and a many buyers are wholesalers.


## Practical Insights and Usage
* Segment and target customers based on their purchase activity and develop or optimise marketing strategies to improve customer acquisition, retention and reactivation
* Identify and profile High-Value Customers (based on their LTV) and target to acquire customers having similar profiles


## Model Input Variable Definitions
* Frequency - count of repeat purchases/contributions
* Recency - duration between a customer’s first contribution/purchase and latest one
* Time (T) - age of a customer within the chosen time unit. This is equal to the duration between a customer’s first contribution/purchase and the end of the period under study
* Monetary Value - the value of each purchase/contribution 


## Model Output
BG/NBD model predicts the following:
* Number of purchases one will make in k future periods
* Probability of one being active at the end of the observation period
   - The p(alive) is calculated based on the recency and frequency of a customer
       - If frequency of purchase is high and recency (time difference between first and last purchase) is high, p(alive) is high
       - If frequency of purchase is low and recency (time difference between first and last purchase) is low, p(alive) is high

Gamma-gamma model predicts the following:
* Average transaction value & lifetime value (LTV) of customer over the set period and set monthly discount rate


## Model Assumptions

BG/NBD Model
1. While active, the number of transactions made by a customer follows a Poisson process with transaction rate (lambda). This is equivalent to assuming that the
time between transactions is distributed exponentialvwith transaction rate (lambda)
2. Heterogeneity in  follows a gamma distribution.
3.After any transaction, a customer becomes inactive with probability p. Therefore the point at which the customer “drops out” is distributed across transactions according to a (shifted) geometric distribution
4. Heterogeneity in p follows a beta distribution
5. The transaction rate  and the dropout probability p vary independently across customers.


Gamma-Gamma Model
* The monetary value of a given transaction of customer varies randomly around their average transaction value
* The average transaction value varies across customers but do not vary over time for any given customer
* The distribution of average transaction values across customers is independent of the transaction process


## Model Limitations
* Based on the paper on BG/NBD model ("Counting Your Customers" the Easy Way), "the BG/NBD model forecasts tend to be relatively poor when penetration and/or purchase frequency are extremely low. In a world where active buyers are either uncommon or very slow in making their purchases, BG/NBD will be outperformed by the Pareto/NBD model. In this case, the one-time buyers (~28% of customers) were removed before fitting the models. 

* Pareto/NBD model will be fitted and compared in another repository.

