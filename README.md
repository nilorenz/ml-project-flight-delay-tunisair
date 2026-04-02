# Machine Learning Flight Delay Project Tunisair

This repository is for the Machine Learning Flight Delay Project with data for predicting flight delays for Tunisair flights.

## Data Origin

Data originally available on zindi: https://zindi.africa/competitions/flight-delay-prediction-challenge

## Collaborators and Team

Christian, Jan and Niklas

## ------------------------------------------------------------------

# Machine Learning Flight Delay Project Tunisair

This project focuses on predicting flight delays for TunisAir using historical flight data. The goal is to build a regression model that estimates the arrival delay (in minutes).

## Collaborators and Team

Christian, Jan and Niklas

## Data Origin

Data originally available on zindi: https://zindi.africa/competitions/flight-delay-prediction-challenge


## Tech Stack:

Language: Python

Libraries: 

Pandas & NumPy: Data manipulation and cleaning.

Seaborn: Exploratory Data Analysis (EDA) and visualization.

Scikit-Learn: Preprocessing and baseline modeling (ElasticNet).

XGBoost & RandomForest: Advanced ensemble methods for regression.

## Workflow & Methodology

1. Exploratory Data Analysis (EDA)

    Visualization of flight frequencies and delay distributions.

    Identification of extreme outliers in the delay minutes.

    Analysis of the relationship between departure/arrival stations and delay times.

2. Preprocessing

    One-Hot-Encoding: Since the dataset consists of categorical features, One-Hot-Encoding was applied to transform these strings into a numerical format suitable for machine learning models.

    Data Splitting: The data was split into training and testing sets using a fixed RSEED = 42 to ensure the reproducibility of all experiments.

3. Model Development & Comparison

    The project evaluates multiple regression strategies:

    ElasticNetCV: Used as a regularized linear baseline to handle potential multicollinearity in encoded features.

    Random Forest Regressor: An ensemble approach to capture non-linear dependencies between routes and delays.

    XGBoost Regressor: A high-performance Gradient Boosting model, further optimized for the specific challenges of the dataset.

4. Hyperparameter Tuning

    The XGBoost model was optimized using RandomizedSearchCV with a comprehensive grid:

    Parameters tuned: n_estimators, learning_rate, max_depth, gamma, subsample, and regularization terms (reg_alpha, reg_lambda).

    Objective Function: reg:squarederror.

## Results

The models were evaluated using Root Mean Squared Error (RMSE) and the R² Score.

The optimized XGBoost model achieved a best RMSE of 38.76.

The R² score of 0.18 reflects the difficulty of predicting delays solely based on schedule data, as many delays are caused by external, stochastic factors like weather or unplanned technical maintenance.