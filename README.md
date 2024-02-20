# Project Title: Feature Engineering and Deep Learning Classification for S&P 500 Direction Prediction

## Overview:
This project encompasses feature engineering and the development of a deep learning classification model to predict the direction of the S&P 500 index. The feature engineering section introduces 12 unique types of features, categorized into Transforming, Interacting, Mapping, and Extracting, aimed at enhancing the predictive power of the model. Subsequently, a Convolutional Neural Network (CNN) is implemented using the Keras library for binary classification, predicting whether the S&P 500 index will move up or down.

## Feature Engineering:
The feature engineering segment introduces 12 types of features designed to capture different aspects of the financial data:

1. **Transformation:**
    - **Robust Scaling:** Applies robust scaling to the data, preserving the original columns' information.
    - **Standard Scaling:** Normalizes the features to have a mean of 0 and a standard deviation of 1.
    - **Square Values:** Applies a square operation to specified columns, enhancing non-linear relationships.

2. **Interaction:**
    - **Ratio of S&P 500 to EuroStoxx 50:** Analyzes relative strength between the S&P 500 and EuroStoxx 50 indices.
    - **Relative Strength of Small-Cap to Large-Cap Stocks:** Examines the relative strength between small-cap and large-cap stocks.
    - **Yield Curve Slope:** Analyzes the slope of the yield curve using 10Y and 2Y Treasury yields.

3. **Mapping:**
    - **Momentum Score:** Calculates the momentum score based on the rate of change in the S&P 500 index.
    - **Relative Strength Index (RSI) of S&P 500:** Computes the RSI for the S&P 500 index.
    - **PCA FTSE Feature:** Applies PCA to create new features based on variance and drops the FTSE column.

4. **Extracting:**
    - **Mean Absolute Change:** Calculates the mean absolute change in the S&P 500 column.
    - **Last Quarter's Rolling Mean:** Computes the rolling mean for the FTSE over the last quarter.
    - **Last 30 Days Return:** Calculates the last 30-day returns for the S&P 500.

## Deep Learning Binary Classification:
A CNN is employed for binary classification to predict the direction of the S&P 500 index. Key steps in this section include:

- Preprocessing the data by creating a binary target variable based on the percentage change in FTSE values and handling missing values.
- Splitting the data into training and testing sets.
- Scaling the data and reshaping it for model input.
- Constructing a Sequential CNN model with convolutional and dense layers.
- Compiling the model with appropriate loss and optimization functions.
- Training the model and evaluating its performance using ROC(AUC) score and accuracy.

## Results:
The CNN model yielded a ROC(AUC) score of 0.5129 and an accuracy score of 0.4854 on the testing data. While the model performed slightly better than random guessing, it demonstrated limited ability to distinguish between the two classes, indicating room for improvement.
