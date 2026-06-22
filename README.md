# House Price Prediction — Supervised Learning

A supervised learning project built as part of a real estate analytics internship. The goal is to predict house prices using multiple regression models, evaluate their performance, and understand the tradeoffs between model complexity, bias, and variance.

# Project Summary
The dataset contains 4200 house records with features like area, number of rooms, location score, distance from the city, and amenities. Several models are trained and compared — from a simple single-feature regression all the way to polynomial regression — with gradient descent implemented from scratch to understand how optimization works under the hood.
Best result: Polynomial Regression (degree 2) using all features achieved a Test R² of ~0.97, with MLR being the most interpretable model at R² ~0.92.

# Project Structure
house-price-prediction-supervised-learning/
│
├── sv_learning_dataset.xlsx       # Dataset (4200 house records)
├── sv_learning_project.ipynb      # Main Jupyter Notebook (complete solution)
└── README.md                      # Project documentation

# Dataset Features
<img width="572" height="480" alt="image" src="https://github.com/user-attachments/assets/7edf6f3a-95c4-472c-a3dc-0d5150044af4" />

# Workflow

Part A — Theory

Covers foundational concepts: supervised learning, regression vs classification, linear regression assumptions, bias-variance tradeoff, and overfitting/underfitting.

Part B — Data Preparation

Loaded and explored the dataset
Checked for missing values (none found)
Identified independent and dependent variables
Visualized feature relationships using scatter plots, correlation heatmap, and boxplots
Split data into 80% training and 20% testing sets

Part C — Simple Linear Regression

Trained SLR using only area_sqft as the predictor
Plotted the regression line
Interpreted the slope and intercept
Validated assumptions using residual plots, Q-Q plot, and scale-location plot

Part D — Model Evaluation

Evaluated SLR using:

Mean Squared Error (MSE)
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
R² Score
Adjusted R² Score

Part E — Multiple Linear Regression

Trained MLR using all 10 features
Compared performance with SLR
Visualized feature coefficients and actual vs predicted plots

Part F — Polynomial Regression

Implemented polynomial regression (degree 2 and 3) on area_sqft
Compared linear vs polynomial curves visually and numerically
Identified overfitting using a degree sweep (degree 1 to 8)

Part G — Gradient Descent Optimization

Implemented all three variants from scratch using NumPy:

Batch Gradient Descent — uses all samples per update
Stochastic Gradient Descent (SGD) — uses one sample per update
Mini-Batch Gradient Descent — uses small batches (size 32)
Compared convergence curves and training time across all three

Part H — Bias–Variance Diagnostics

Computed Train R² and Test R² for all four models
Plotted and compared the train-test gap (bias-variance tradeoff)
Identified the model with the best balance

Part I — Final Report

Summarized all findings
Identified best model and why
Discussed gradient descent impact
Provided practical business interpretation of results
<img width="642" height="262" alt="image" src="https://github.com/user-attachments/assets/7c91cdd7-2daf-4976-a408-c84db5a71590" />

# Key Findings
area_sqft and location_score are the strongest predictors of house price.
distance_city_km and age_years have a negative effect on price.
MLR dramatically outperforms SLR by using all available features.
Polynomial Regression (degree 2) achieves the best test accuracy with minimal overfitting.
Mini-Batch Gradient Descent is the most efficient optimization method among the three tested.

# Tech Stack

Python 3.x
pandas, numpy
matplotlib, seaborn
scikit-learn
scipy

