# Weather Temperature Prediction
# Dataset Description
The "Weather Type Classification" dataset includes various weather-related variables described as follows:

*    **Temperature (numeric):** The temperature in degrees Celsius, ranging from extreme cold to extreme heat.
*   **Humidity (numeric):** The humidity percentage, including values above 100% to introduce outliers.
*   **Wind Speed (numeric):** The wind speed in kilometers per hour, with a range including unrealistically high values.
*   **Precipitation (%) (numeric):** The precipitation percentage, including outlier values.
*   **Cloud Cover (categorical):** The cloud cover description.
*   **Atmospheric Pressure (numeric):** The atmospheric pressure in hPa, covering a wide range.
*   **UV Index (numeric):** The UV index, indicating the strength of ultraviolet radiation.
*   **Season (categorical):** The season during which the data was recorded.
*   **Visibility (km) (numeric):** The visibility in kilometers, including very low or very high values.
*   **Location (categorical):** The type of location where the data was recorded.
*   **Weather Type (categorical):** The target variable for classification, indicating the weather type.

The dataset was obtained from https://www.kaggle.com/datasets/nikhil7280/weather-type-classification/data and was augmented with missing values and duplicate records to better suit the task.
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

![Beobachtete vs Vorhergesagte Temperaturen](Beobachtete_vs_Vorhergesgte_Temperaturen.PNG)
