# Bike Rental Demand Prediction
This project involves predicting bike rental demand prediction using historical data. The goal is to build a machine learning model that can estimate the number of rental bikes, helping bike rental companies optimize inventory and improve customer satisfaction.

## Project Overview
Bike rental systems are gaining popularity in urban areas as they offer an eco-friendly and convenient transportation alternative. However, rental companies often face challenges in predicting demand, which can lead to overstocking or shortages. This project addresses this problem by developing a predictive model to estimate bike rental demand based on various features such as weather conditions, time of day, and seasonality.

## Dataset
### Features
The dataset used in this project contains historical rental bike data, including the following features:

- Date and Time: The hour and date of the rental.

- Weather Information: Temperature, humidity, and weather conditions.

- Seasonality: Hour, day, month, and year.

- Holiday and Working Day Indicators: Whether the day is a holiday or a regular working day.

### Target
- Count: The number of rental bikes demanded in a given hour (1-970, right-skewed).

## Modeling Process
Data Preprocessing:
- Handling missing values, encoding categorical features, and scaling numerical features.
- Transforming temporal features (e.g., sine and cosine encoding for hours).
Model Selection:
- The primary model used is XGBoostRegressor, chosen for its efficiency and ability to handle non-linear relationships.
Hyperparameter Tuning:
- Parameters like max_depth, eta, gamma, n_estimators, and subsample were optimized using grid search and cross-validation.

## Evaluation Metrics
The model performance is evaluated using:
- Root Mean Squared Error (RMSE): Measures the average magnitude of prediction error. Lower values indicate better performance.
- Mean Absolute Error (MAE): The average absolute difference between predicted and actual values. Used as the primary metric.
- Mean Absolute Percentage Error (MAPE): The average percentage error in predictions.
Performance Results:
- Before Tuning:
  - RMSE: 40.4
  - MAE: 25.4
  - MAPE: 45%
- After Tuning:
  - RMSE: 37.7
  - MAE: 22.9
  - MAPE: 34%

## Conclusion
- The most influential features are: hour, year, temperature, season
- The model struggles with high-demand scenarios (count > 400) but performs well for typical rental counts.
- Post-tuning improvements highlight the importance of optimizing hyperparameters for better prediction accuracy.

This project showcases the potential of machine learning in solving practical business challenges and demonstrates how predictive models can enhance decision-making in real-world scenarios.
