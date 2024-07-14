Google Stock Price Prediction


Introduction


This project focuses on predicting Google stock prices using historical data and various machine learning techniques. The primary aim is to develop a model that accurately forecasts stock prices, aiding investors and analysts in making informed decisions.


Table of Contents


*Introduction


*Dataset


*Installation


*Data Preprocessing

*Exploratory Data Analysis (EDA)


*Feature Engineering


*Modeling


*Evaluation


*Conclusion


Dataset


The data for this project is fetched from Yahoo Finance using the yfinance library. It includes historical stock prices for Google (GOOGL) over the maximum available period.


Installation


To run this project, you need to have the following libraries installed:

numpy


pandas


matplotlib


seaborn


yfinance


xgboost


scikit-learn


imblearn


tensorflow



Data Preprocessing


Data Collection: Historical stock prices are fetched using the yfinance library.


Target Variable: A target variable is created to indicate whether the closing price has increased compared to the previous day.


Resampling: The data is resampled to balance the classes.


Exploratory Data Analysis (EDA)


Month-wise and Day-wise Averages: Visualizations of month-wise and day-wise average stock prices.


Time Series Plots: Plots of stock prices over time for different features (Open, High, Low, Close, Volume).


Candlestick Chart: A candlestick chart is plotted for the last two years to visualize stock price movements.


Class Distribution: The distribution of the target variable before and after resampling is visualized.


Feature Engineering


New features are engineered to capture trends and ratios:



Rolling Means: Weekly, quarterly, and annual rolling means of the closing prices.


Trend Indicators: Weekly trend and ratios between different rolling means.


Ratios: Ratios of open, high, and low prices to the closing prices.


Modeling


A GRU (Gated Recurrent Unit) model is used for time series prediction. The data is scaled using MinMaxScaler, and a sequential neural network model is built using TensorFlow and Keras. The model architecture includes:


Input Layer


GRU Layer


Dense Layers


Evaluation


The model is evaluated using Mean Squared Error (MSE) and Root Mean Squared Error (RMSE). Predictions are plotted against actual values to visualize the model's performance over time.


Prediction vs Actuals: A plot showing the model's predictions against the actual stock prices.


Conclusion


This project demonstrates the process of stock price prediction using machine learning techniques. The GRU model provides a framework for forecasting stock prices, though further tuning and feature engineering can enhance its accuracy.
