# Bike-Sharing Demand Prediction

## Overview

This project aims to predict bike-sharing demand using a multiple linear regression model. The dataset consists of 730 rows and 16 columns, representing two years of data for a bike-sharing company. The goal is to understand the key factors influencing demand and build a predictive model that provides reliable forecasts.

## Exploratory Data Analysis (EDA)

Conducted EDA to understand distributions, correlations, and patterns.

Identified one target variable (cnt) and multiple continuous and categorical independent variables.

## Data Preprocessing

Rescaled continuous variables using MinMaxScaler to normalize data.

Encoded categorical variables using dummy variables for better model performance.

Split the data into training (70%) and testing (30%) sets using train_test_split.

## Feature Selection

Applied Recursive Feature Elimination (RFE) to reduce features from 16 to 10.

Checked for multicollinearity using Variance Inflation Factor (VIF).

Dropped the hum column due to a high VIF value of 10, ensuring all features had VIF < 5.

## Model Building

Linear Regression using Statsmodels OLS

Built a multiple linear regression model using the Ordinary Least Squares (OLS) method.

Observed:

p-values close to 0, indicating statistical significance of features.

R² Score:

80% on training data

77% on test data

Residuals normally distributed and centered around 0, satisfying linear regression assumptions.

## Model Evaluation

### Residual Analysis

Checked residual distribution using seaborn.

Confirmed no significant patterns, indicating a well-fitted model.

### Final Model Performance

Training R² Score: 0.80

Test R² Score: 0.77

The model generalizes well with minimal overfitting.