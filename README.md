--- This repository is coded in Python 3.6 using Jupyter Notebooks ---

# What is Customer Churn?

Customer Churn is used to describe subscribers to a service who decide to discontinue their service for a certain time frame. Churn prediction consists of detecting which customers are likely to cancel a subscription to a service based on how they use the service. 

![Please-Come-Back-Tim-Etchells-Neon-2008-Image-Courtesy-of-the-Artist-72dpi](https://user-images.githubusercontent.com/45079009/84798276-9c060800-afaf-11ea-8f97-7075c264070f.jpg)

# Why it matters?
Businesses often have to invest substantial amounts attracting new clients, so every time a client leaves it represents a significant investment lost. Both time and effort then need to be channelled into replacing them. Being able to predict when a client is likely to leave and offer them incentives to stay can offer huge savings to a business.

# The DATA

![Data](https://user-images.githubusercontent.com/45079009/84798960-70375200-afb0-11ea-8d46-ac7f0579769c.PNG)

The data consisted of 7 numerical variables, 2 categorical, 2 date and 1 boolean.

# Exploring the data

Distribution of means of all numerical variables indicated data needed to be scaled before modelling.
![mean](https://user-images.githubusercontent.com/45079009/84799160-b68cb100-afb0-11ea-98e5-4b5d51228486.PNG)

Android users experiencing higher surge than iPhone users
![surge](https://user-images.githubusercontent.com/45079009/84799510-361a8000-afb1-11ea-9146-ae1e6824652a.PNG)

Correlation between features
![corr](https://user-images.githubusercontent.com/45079009/84799679-7aa61b80-afb1-11ea-9929-d525a3b63fd3.png)

# Models Used:
- 1. Logistic Regression
- 2. Decision Tree
- 3. Random Forest
- 4. Gradient Boosting
- 5. AdaBoost

# Results

![results_combined](https://user-images.githubusercontent.com/45079009/84800675-fd7ba600-afb2-11ea-8495-0d740132925f.PNG)

# Tuning parameters for Gradient Boosting and Ada-Boost

1. Number of estimators
2. Learning Rate
3. Maximum depth

# Optimized Results

![tuned combined roc](https://user-images.githubusercontent.com/45079009/84801290-d5d90d80-afb3-11ea-84f2-1df9da433979.PNG)

# The cost curve

The curve is obtained using the Gradient Boosted model.

![cost curve](https://user-images.githubusercontent.com/45079009/84801455-0d47ba00-afb4-11ea-9560-2316957e0ad8.PNG)

- This chart shows that picking a low threshold works in the best interest as 63% of customers are churning (previously observed!). If we give all the customers a retention incentive, it would cost us around USD 200,000. However, with this model and the threshold of 0.26, the overall cost can be minimized at USD 183,720. The graph also shows, how not taking any action would be disastrous as the costs are sky-rocketing at USD 438,130.

# Factors affecting customers to churn

![imp features](https://user-images.githubusercontent.com/45079009/84801613-3ec08580-afb4-11ea-9c46-a0a89010e6a1.PNG)

# Final Take:

Not taking any action on the customers, would cost the company a lot of money- around USD 438,000. With usage of the model and analysis, company can reach out to the churning customers with incentives and minimize the cost to USD 183,000.

- Also, Android users are expriencing a higher surge charge compared to iPhone users - and that is causing them to churn.
- Customers in Astapor are churning more and King's Landing are less likely to churn.
- Also, company should promote usage of luxury_car in the first 30 days as it is promoting retention.
- Finally, riding during the week and ratings provided by the driver are important factors to look for to identify churning customers.


#### - Extensions
- Some customers who receive retention incentives will still churn. Including a probability of churning despite receiving an incentive in our cost function would provide a better ROI on our retention programs.
- Actual training data and monetary cost assignments could be more complex.
- Multiple models for each type of churn could be needed.

