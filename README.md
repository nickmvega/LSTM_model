# INTRODUCTION

This project aims to predict Apple Inc. (AAPL) stock price movements using a comprehensive data-driven approach. The model is built on a robust feature set incorporating correlated assets, technical indicators, Fourier transforms, and ARIMA models, all processed and visualized using pandas and matplotlib.

The core of the model is a Long Short-Term Memory (LSTM) network, specifically designed for time-series forecasting. Through Bayesian optimization, the hyperparameters of the LSTM model are fine-tuned to improve accuracy and performance, enabling the model to effectively capture temporal dependencies and market patterns in an increasingly complex financial landscape.

The entire pipeline is in Stock_Prediction_Model.ipynb

# RESULTS

The model achieved an RMSE (Root Mean Squared Error) of 0.0474 and an MAE (Mean Absolute Error) of 0.0370, indicating a relatively low error rate in predicting the stock prices of Apple Inc. (AAPL). The RMSE measures how much the predictions deviate from the actual values on average, while the MAE reflects the average magnitude of errors in the predictions.

A visual of the predictions can be seen in Apple Predictions.png.
