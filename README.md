# 🚗 Car Price Prediction using Linear Regression
## Overview

This project builds a baseline Machine Learning regression model to predict the selling price of used cars in the Indian market using historical data and vehicle specifications.

The objective of this project is learning-focused:

To understand the complete ML pipeline

To implement Simple & Multiple Linear Regression correctly

To handle real-world data issues such as skewness, missing values, and categorical variables

To evaluate regression models using appropriate metrics and diagnostics

This project is intentionally scoped as a baseline model, not a production-optimized system.

## Problem Statement

The Indian used-car market lacks a standardized pricing mechanism.
Prices for similar cars vary significantly due to subjective valuation, information asymmetry, and inconsistent market knowledge.

This creates challenges for:

Sellers, who may underprice or overprice vehicles

Buyers, who struggle to identify fair market value

The goal of this project is to predict a fair selling price for used cars based on historical data and vehicle attributes.

## Dataset

Source: CarDekho (Kaggle)

Rows: ~8,100

Features: 13

Target Variable: selling_price

## Key Features

Year of manufacture

Kilometers driven

Fuel type

Seller type

Transmission

Ownership history

Mileage, engine capacity, and power (cleaned from text)

Brand (extracted from vehicle name)

## Key Challenges Addressed

Mixed data types (numeric values stored as strings with units)

Missing values in multiple columns

Highly skewed target variable (selling_price)

High-cardinality categorical features (car brands)

Multicollinearity between technical features

Outliers due to luxury vehicles

## Approach
### 1. Data Cleaning & Preprocessing

Extracted numeric values from text columns (mileage, engine, max_power)

Handled missing values

Dropped torque due to inconsistent formatting and limited practical value

Extracted car brand from vehicle name

One-hot encoded nominal categorical features

Ordinal encoded ownership history

### 2. Feature Transformation

Applied log transformation to:

selling_price

km_driven

Reduced skewness and improved regression assumptions

### 3. Model

Multiple Linear Regression

Used as a baseline model for interpretability and learning

Train–test split based evaluation

### Evaluation Metrics

R² Score

Adjusted R²

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Model Performance (Test Set)

R²: ~0.80+

Adjusted R²: ~0.78+

Residuals approximately normally distributed after log transformation

Predictions closely aligned with actual values for low-to-mid priced cars

### Note: Error metrics are computed in log-space due to target transformation.

### Visual Diagnostics

Actual vs Predicted plot

Residual distribution

Model behavior across price ranges

These plots were used to validate regression assumptions and detect bias.

### Project Scope & Limitations
#### What This Project Covers

SLR & MLR implementation

Feature engineering

Encoding strategies

Log transformations

Model evaluation & diagnostics

#### What Is Intentionally Not Included

Cross-Validation

VIF-based feature elimination

Regularization (Ridge / Lasso)

Hyperparameter tuning

Tree-based or ensemble models

These topics will be explored in future iterations once the concepts are formally covered.

### Future Improvements

Add cross-validation for robust evaluation

Apply Ridge and Lasso regression

Perform systematic feature selection using VIF

Compare with tree-based models (Random Forest, Gradient Boosting)

Convert predictions back to original price scale for business interpretation

Deploy model using Flask or Streamlit

## Learning Outcome

This project represents a solid baseline regression model built with disciplined ML practices.
It is intended to demonstrate understanding, decision-making, and clean implementation, not aggressive optimization.

## Author

Manoj Anil Sabale
B.E. Artificial Intelligence & Data Science
Focused on building strong ML fundamentals before optimization

## 📌 Final Note (Important)

This repository documents a learning milestone, not an end state.
Future versions will build upon this baseline as more advanced concepts are learned.
