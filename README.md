# Housing-Price-Prediction

## Overview
This document provides documentation for a project aimed at predicting housing prices. The project utilizes a dataset containing various features related to houses, including square footage, number of bedrooms, location, and more. The primary objective is to build regression models to predict house prices based on these features.

## Dataset Overview
The dataset consists of the following columns:

1. id: Unique identifier for each house.
2. date: Date the house was sold.
3. price: Price of the house (target variable).
4. bedrooms: Number of bedrooms.
5. bathrooms: Number of bathrooms.
6. sqft_living: Square footage of the living area.
7. sqft_lot: Square footage of the lot.
8. floors: Number of floors.
9. waterfront: Whether the house has a waterfront view (binary: 0 for no, 1 for yes).
10. view: Index from 0 to 4 representing the house's view.
11. condition: Index from 1 to 5 representing the house's condition.
12. grade: Index from 1 to 13 representing the house's grade.
13. sqft_above: Square footage above ground.
14. sqft_basement: Square footage of the basement.
15. yr_built: Year the house was built.
16. yr_renovated: Year the house was renovated.
17. zipcode: ZIP code of the location.
18. lat: Latitude of the location.
19. long: Longitude of the location.
20. sqft_living15: Living room area in 2015 (implies some renovations).
21. sqft_lot15: Lot size area in 2015 (implies some renovations).

 ## Data Cleaning and Exploration
The initial steps involved examining the dataset, checking for missing values, and exploring basic statistics. The dataset contains 21,613 entries, and there are no duplicates. The 'date' column was converted to a datetime format for better analysis.

### Features and Target Variable
The dataset includes both numerical and categorical features. The target variable is 'price.' Numerical features include square footage, number of bedrooms and bathrooms, etc. Categorical features include 'waterfront,' 'view,' 'condition,' and 'grade.'

## Exploratory Data Analysis (EDA)
EDA was performed to understand the distribution of key variables and their relationships. Key insights include:

- Most houses have one or two floors.
- The distribution of house prices varies for those with and without a waterfront view.
- The 'sqft_above' feature is positively correlated with house prices.

## Building Regression Models

### Linear Regression with Single Feature
A simple linear regression model was built to predict house prices using the 'sqft_living' feature. The model achieved an R^2 value of approximately 0.49.

### Linear Regression with Multiple Features
A multiple linear regression model was trained using various features such as 'floors,' 'waterfront,' 'lat,' 'bedrooms,' etc. The R^2 value for this model is approximately 0.66.

### Ridge Regression
Ridge regression was employed to handle potential multicollinearity in the multiple linear regression model. The model, with regularization parameter (alpha) set to 0.1, achieved an R^2 value of approximately 0.66.


### Polynomial Transformation with Ridge Regression
To capture non-linear relationships, a second-order polynomial transformation was applied to the features, followed by Ridge regression. The resulting model achieved an improved R^2 value of approximately 0.71.

## Conclusion
The project successfully built regression models to predict housing prices based on various features. The models provide valuable insights into the impact of different features on house prices. Further refinements and optimizations can be explored to enhance model performance.

For detailed implementation and code, please refer to the associated Jupyter notebook or script.
	



	

