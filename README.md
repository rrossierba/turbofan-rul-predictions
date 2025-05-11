# TurboFan Engine Remaining Useful Life (RUL) Prediction

Data source: https://www.kaggle.com/datasets/behrad3d/nasa-cmaps/data

## Overview

This project focuses on predicting the Remaining Useful Life (RUL) of turbofan engines using various machine learning models. By leveraging historical sensor data, the project aims to enhance maintenance strategies for aircraft engines, making them more efficient and cost-effective.

## Data Description

The dataset consists of multivariate time series representing different turbofan engines, each beginning with varying degrees of initial wear and manufacturing variations. Each time series captures operational settings and sensor measurements that are indicative of engine performance and degradation over time.

## Methodology

### Data Preprocessing

1. **Cleaning**: Removal of columns with constant values and low correlation with the target variable.
2. **Smoothing**: Applied smoothing techniques to reduce noise in sensor data.
3. **Clipping RUL**: RUL values were capped to handle outliers effectively and to better correlate with sensor data trends.

### Machine Learning Models

- **Linear Regression**: A baseline model to capture linear relationships.
- **Elastic Net**: Combines L1 and L2 regularization to improve generalization.
- **Regression Trees**: Non-linear model using decision tree regression.
- **Support Vector Machines (SVM)**: Both linear and RBF kernels to capture complex relationships.
- **Random Forests**: An ensemble method showing superior performance in capturing data complexity.
- **Neural Networks**: Used for capturing non-linear patterns, though performed less effectively on the dataset size.

### Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

## Results

The Random Forest model provided the best performance on test data with high accuracy and robustness, making it a suitable choice for RUL prediction tasks. The SVM with RBF kernel also demonstrated strong performance, particularly in capturing non-linear relationships.

Ensemble methods like Random Forests and advanced models like SVM with RBF kernel significantly improve the reliability of RUL predictions over simpler models such as Linear Regression. Future work could include more detailed hyperparameter tuning and exploration of advanced deep learning architectures.

## Future Work

- Integration of Recurrent Neural Networks (RNNs) for time-series predictions.
- Expansion of the dataset with additional sensor measurements and operational settings.
- More sophisticated feature engineering techniques to enhance model performance.
