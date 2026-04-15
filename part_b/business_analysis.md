# B1 (a): Problem Formulation

## Target Variable
The main goal is to predict `items_sold`, which represents how many items are sold in a store during a particular month.

## Input Features
To make this prediction, we can use the following inputs:
- Store details: store_size, location_type, store_id  
- Promotion type: promotion_type (discount, BOGO, free gift, etc.)  
- Time-related factors: month, weekend, festival  
- Competition: competition_density  
- Customer-related factors: footfall, demographics  

## Type of Machine Learning Problem
This is a Regression Problem.

## Justification
The objective is to predict the number of items sold, which is a continuous numerical value. Since the output is numeric and not categorical, regression is the appropriate machine learning approach.

Using this model, the business can estimate sales for different promotions and select the most effective promotion for each store.

## Simple Understanding
We are predicting “how many items will be sold”, so this is a regression problem.

## B1 (b): Target Variable Justification

## Why items_sold is a Better Target than Revenue

Using `items_sold` (sales volume) is more reliable than total sales revenue because revenue can be influenced by multiple external factors such as pricing, discounts, and product mix.

For example, a promotion may increase the number of items sold but reduce revenue due to heavy discounts. In such cases, revenue does not accurately reflect the true effectiveness of the promotion. On the other hand, `items_sold` directly measures customer response and demand, making it a more stable and meaningful indicator for evaluating promotion performance.

## Broader Principle

This illustrates an important principle in machine learning:  
the target variable should closely align with the actual business objective and should not be heavily affected by external or confounding factors.

Choosing the right target variable ensures that the model learns meaningful patterns and provides reliable, actionable insights.

# B1 (c): Alternative Modelling Strategy

Instead of using a single global model for all stores, a better approach is to use **segmented or grouped models** based on store characteristics such as location type (urban, semi-urban, rural).

Stores in different locations often have different customer behavior, competition levels, and purchasing patterns. Because of this, the same promotion may have varying effects across stores.

By building separate models for each segment (or including interaction effects between store type and promotion), the model can better capture these differences and provide more accurate predictions.

## Justification
This approach improves model performance by accounting for data heterogeneity. It allows the model to learn location-specific patterns rather than forcing a single model to generalize across very different store environments.