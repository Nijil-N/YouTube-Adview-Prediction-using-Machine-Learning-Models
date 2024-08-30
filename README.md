# YouTube-Adview-Prediction-using-Machine-Learning-Models
This project is done based on regression models

## Overview

The goal of this project is to build predictive models to estimate the number of adviews a YouTube video will receive based on various features. The dataset used for this prediction includes features such as views, likes, dislikes, comments, and video categories. The models trained and evaluated in this project include Linear Regression, Decision Tree Regressor, and Random Forest Regressor.

## Dataset

The dataset, `train.csv`, contains historical data on YouTube videos, including:
- `views`: The number of views a video has received.
- `likes`: The number of likes a video has received.
- `dislikes`: The number of dislikes a video has received.
- `comment`: The number of comments on a video.
- `adview`: The target variable indicating the number of adviews.
- `category`: The category of the video.
- `vidid`: A unique identifier for the video.
- `published`: The publication date of the video.

## Data Preprocessing

1. **Outlier Removal:** Data points with `adview` values greater than 2,000,000 are removed to prevent skewness.
2. **Handling Missing Values:** Rows with 'F' in columns related to views, likes, dislikes, or comments are removed as they likely contain missing or erroneous data.
3. **Data Conversion:** Non-numeric columns are converted to numeric format to facilitate model training.
4. **Categorical Encoding:** Categorical features are encoded into numerical values for compatibility with machine learning models.

## Model Training and Evaluation

### Linear Regression

- **Purpose:** To understand the linear relationship between the features and adviews.
- **Evaluation:** Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE) are used to measure model performance.
- **Visualization:** Line plots and QQ plots are used to compare actual vs. predicted adviews and assess residuals.

### Decision Tree Regressor

- **Purpose:** To capture non-linear relationships and interactions between features.
- **Evaluation:** Error metrics such as MAE, MSE, and RMSE are computed to evaluate the model.
- **Visualization:** Line plots and QQ plots for residuals help in visualizing model predictions and error distribution.

### Random Forest Regressor

- **Purpose:** To improve prediction accuracy by combining multiple decision trees.
- **Evaluation:** MAE, MSE, and RMSE provide insights into model performance.
- **Visualization:** Line plots and QQ plots help in comparing the predicted adviews with actual values and analyzing the residuals.

## Model Saving

The trained models are saved using `joblib` for future use and deployment. This allows for the models to be loaded and used for predictions on new data without needing to retrain them.

- **Decision Tree Model:** Saved as `decisiontree_youtubeadview.pkl`.
- **Random Forest Model:** Saved as `randomforest_youtubeadview.pkl`.

## Summary

This project demonstrates the process of predicting YouTube adviews using various regression models. It involves data preprocessing, model training, evaluation, and visualization to assess and improve model performance. The chosen models are Linear Regression, Decision Tree Regressor, and Random Forest Regressor, each providing different insights and performance metrics for predicting adviews.
