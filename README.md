# Sales Predictions
## Analysis of sales & what has meaningful impact on them.

**Author**: Michael Clausen

### Business problem:

Analyze and determine what is affecting sales, predict how they can change in the future.


### Data:
**Source**: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

This Data Set has 12 columns and 8523 rows.

### Data Dictionary

![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/datadict.jpg)

### To prepare this data, it was cleaned, and the following steps were taken to help analyze it:

#### Exploratory Data Analysis
- During exploratory Data analysis Barplots are used to help anayzle all the data.

##### Outlet Type VS. Average Sales
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/Outlet%20type%20vs%20mean%20of%20sales.png)

> This visualization shows us which outlet has the highest average sales.


#### Explantory Data Analysis
-To visulaize data a barplot was made to show the average sales, of individual Item Types.

##### Mean of Sales compared to Item Types
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/SalesvsItemtype.png)

> This visualization shows us what products have the highest average sales. Starchy Foods have the highest average sales.


## Machine Learning Using the Following Models
- Linear Regression Model
- Random Forest Regressor Model
- Decision Tree Regressor Model
- Bagged Tree Model


## Models Evaluted & Results


##### Linear Regression Test Scores
- MAE: 804.1430 
- MSE: 1,194,371.4977 
- RMSE: 1,092.8730 
- R2: 0.5671

##### Decision Tree Regressor Test Scores
- MAE: 738.3173 
- MSE: 1,118,185.9731 
- RMSE: 1,057.4431 
- R2: 0.5947

##### Bagging Regressor Test Scores
- MAE: 767.3214 
- MSE: 1,219,027.1669 
- RMSE: 1,104.0956 
- R2: 0.5582

##### Random Forest Regressor Test Scores
- MAE: 728.3901 
- MSE: 1,096,396.4989 
- RMSE: 1,047.0895 
- R2: 0.6026


#### The final Model Chosen is Random Forest Regressor Model with the depth set to 5.

- For the testing set on the model, 60% of the variance in y was explained by x
- The Mean Absolute Error was off by about $728
- The Mean Squared Error was $1,096,396.50
- The Root Mean Squared Error was calculated at $1,047.08

## Recommendations:

### Overall Recomendations

*   Starchy foods sell the highest amount on average.
*   Supermarket Type3 has the highest sales average of all outlet_types.


### Model Recomendation

*   Overall the best option is the tuned Forest Regressor Model, Little Bias. Still had some but far less than other models used.

### Final Recomendation

*   Using this model to make predictions about sales will not be very reliable, considering previous metrics from how the model performed there is a disparity between R^2 and Root Mean Squared Error that is not negligible.

## Limitations & Next Steps

- From here a business could use this to see that certain, foods and outlet types do sell better on average.



## Coefficients and Importances

### Coefficients
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/coefficients.png)
*  This Feature intercept has a positive impact on the target variable.
*  This Feature Outlet_Type_Grocery Store has a negative impact on the target variable.
*  This Feature Outlet_Identifier_OUT027 has a positive impact on the target variable.

### Importances Random Forest
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/importances.png)
* Item_MRP, is the most important feature, It represents the maximum price the product can be sold to the customer.
* Item_Visibility, Items viewability in the store greatly impacts sales.
* Outlet Type, Shows that different outlet types have higher sales counts.

## Summary Plots
### Bar
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/shap.png)

### Dot
![Alt text](https://github.com/MikeyClausen/Prediction-of-Product-Sales/blob/main/shapdot.png)

* Outlet_Type_Grocery store: Grocery store type has the best sales.
* Item_MRP: Effects the model in both ways. 
* Outlet_Identifier_OUT027: Highest selling store.
