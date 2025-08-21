# House Price Prediction (Machine Learning Regression Model)

## Introduction
**Inspiration :** This project was in inspiration of my first hackathon I participated in. Despite receiving a top 5 overall RMSE score and presenting our solution to a panel of judges, I wanted to deepen my understanding of the machine learning workflow.
<br>
<br>
**Defining the problem :** Given a dataset of California Housing Prices, estimate the median house value of houses within a district

## Workflow
1. Split the data into training set using stratified sampling
2. Understand and visualize the data to gain insight
3. Clean the data
4. Create custom transformer
5. Create data preprocessing pipeline
6. Pick and train on a machine learning model
7. Fine tune chosen model
8. Evaluate final model on the test set

## About the features and the dataset
Features within the dataset:
- longitude
- latitude
- housing_median_age
- total_rooms
- total_bedrooms
- population
- households
- median_income
- ocean_proximity
- median_house_value **-> target variable**

Additional features added through feature engineering:
- rooms_per_household
- population_per_household
- bedrooms_per_room

## Data preprocessing:
**Missing data :** 
- Only the numerical data was missing so, using an imputer, we replaced the empty data entry with its column median

**Numerical data :**
- I scale the data using standardization, also called z-score normalization (StandardScaler object)

**Text data :**
- Used OneHotEncoder for the ocean_proximity feature

## Models and evaluation metric used
- Linear Regression
- Random Forest Regressor
- Support Vector Regressor

- RMSE
- RMSE with 95% confidence interval

## Best results
RMSE with 95% confidence interval of [44423.402, 48262.724] (3sf)
