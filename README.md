# E-Commerce-CLV-Prediction

## Introduction 

The e-commerce customer dataset includes 13 variables, such as purchase date, purchase amount, product category, quantity, returns, churn status, and others.

Customer lifetime value (CLV) is a critical metric because it enables businesses to make smarter, data-driven decisions that foster customer loyalty, reduce acquisition costs, and ensure sustainable profitability. As a result, CLV is a cornerstone metric for long-term business success.

The objective of this project is to develop a CLV prediction model. By leveraging this model, the e-commerce company can make strategic decisions based on predicted CLV. For example, discounts can be offered to customers with low predicted CLV to boost engagement, while loyalty programs can be targeted toward high-CLV customers.

## Table of Contents

1. Introduction
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Model Development
5. Feature Importance
6. Conclusion

![workflow](image/WORKFLOW.png)


## Exploratory Data Analysis (EDA)

### Visualization of continuous variables

![EDA1](image/EDA1_revise.png)

![EDA2](image/EDA2.png)

### Churn and return rates show heavily concentrated in any specific variables?

![EDA3](image/EDA3.png)

![EDA4](image/EDA4.png)

### Key Findings

The churn rate is 20%, and the return rate is 50%. These rates are evenly distributed across the following factors:

- Product Category
- Payment Method
- Gender
- Customer Age

Churn and return rates do not appear to be heavily concentrated in any specific feature. Although the churn rate is slightly higher among customers in their 20s and lower among those in their 40s, returns are relatively evenly distributed across age groups.

Therefore, product and service improvements should be implemented broadly rather than targeting specific customer segments or products.

## Feature Engineering




![FEATUREENGINEERING](image/FEATUREENGINEERING.png)

1. Create dummy variables to represent categorical variables
2. Group by customers
3. Calculation CLV - (Purchase value X Frequency X Customer lifespan)

*Independent Variable  -> [['Total_returns','Books', 'Clothing', 'Electronics', 'Furniture', 'Payment_Cash','Payment_Credit', 'Payment_Paypal', 'Gender_Female','Age', 'churn']]


*Dependent Variable -> [['CLV']]

## Model Development

![model](image/result.png)

### -

![model2](image/modelresults.png)


## Feature Importance

![featureimportance](image/featureimportance.png)

## Conclusion

To summarize, customer lifetime value (CLV) was predicted using historical transaction features such as product category, payment method, return rate, and others.

Five models—Linear Regression, Decision Tree, Random Forest, Gradient Boosting, and XGBoost—were evaluated for CLV prediction in an e-commerce setting. Among them, the XGBoost model achieved the best performance in terms of MAE, with a value of 9,252, indicating the lowest average prediction error. (Feature importance analysis shows that payment method and return rate contribute the most to the model’s performance.)

Although the linear regression model achieved better RMSE and R² scores, MAE is a more relevant metric for typical customers, and the lower MAE of XGBoost indicates better practical prediction accuracy. Therefore, the XGBoost model is selected as the final model for CLV prediction.



