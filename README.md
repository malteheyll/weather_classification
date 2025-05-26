# Weather Temperature Prediction

This project uses a weather dataset to compare different regression models for temperature prediction.

# Project Overview

1. Data Import & Cleaning

- Load weather_classification_data.csv with Pandas

- Detect and remove outliers using the IQR method

- Impute missing values

-  categorical variables with one-hot encoding

2. Exploratory Data Analysis (EDA)

- Visualize distributions and relationships using histograms and scatter plots

- Examine correlations between features

3. Model Training & Comparison

- Linear Regression as a baseline model

- Random Forest Regressor for capturing non-linear patterns

- LightGBM Regressor with hyperparameter optimization via Optuna

4. Results

- The optimized LightGBM model (n_estimators=220, learning_rate=0.02, max_depth=7, num_leaves=10, min_data_in_leaf=20) achieved the best performance with an  of approximately 0.74.

- Random Forest and Linear Regression achieved  values of about 0.65 and 0.55, respectively.
