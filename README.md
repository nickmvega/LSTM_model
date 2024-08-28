# INTRODUCTION

This project aims to predict Apple Inc. (AAPL) stock price movements using machine learning techniques. The machine learning model is built on a feature set incorporating correlated assets, technical indicators, Fourier transforms, and ARIMA models, all processed and visualized using pandas and matplotlib.

The model is a Long Short-Term Memory (LSTM) network designed explicitly for time-series forecasting. Through Bayesian optimization, the hyperparameters of the LSTM model are fine-tuned to improve accuracy and performance, enabling the model to capture temporal dependencies and market patterns effectively.

The entire pipeline is in Stock_Prediction_Model.ipynb

# THE DATA

A substantial amount of data and various features are essential to predict AAPL stock price movements. This project's dataset consisted of 2,429 days: 1,700 days allocated for training and 729 days for testing.

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/b2f23327fb3a0c7a0e2e351d10954a880894fc0c/Train%3ATest%20Split.png)

The features used were:

**Correlated Assets**: The AAPL stock price can be influenced by the performance of correlated assets, such as other technology companies, indices, and related sectors. These assets provide additional context to market and sector trends. For example, the performance of Amazon or Microsoft can indicate broader industry movements that AAPL might follow, making these correlations valuable predictors.

**Technical Indicators**: Various technical indicators were employed to capture different aspects of the stock's price behavior:

- Simple Moving Averages (SMA): In the context of this project, an SMA calculates the average stock for 7-day and 21-day periods and assigns equal weight to each stock price within those periods. The 7-day and 21-day SMAs smooth out short-term price fluctuations, helping to identify the overall trend direction.

Exponential Moving Averages (EMA): The 12-day and 26-day EMAs are more heavily weighted to recent prices than SMAs, making them more responsive to new information and detecting short-term momentum changes.

- MACD and Signal Line: The Moving Average Convergence Divergence (MACD) and its Signal Line are crucial for identifying changes in a trend's strength, direction, momentum, and duration.

Relative Strength Index (RSI): In the context of this project, the 14-day RSI measures the speed and magnitude of a stock price change, allowing the identification of overvalued or undervalued conditions. An RSI can also indicate stock prices that may exhibit a trend reversal. 

- Bollinger Bands: Bollinger Bands measure volatility by placing standard deviation lines above and below an SMA, identifying overextended price moves that may revert to the mean.

- Momentum: The speed (accelerates or decelerates) at which the price of a stock changes. 

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/Technical%20Indicators%20.png)

**Fourier Transforms**: In the context of this project, Fourier transforms were utilized to extract underlying trends by breaking the price series into trigonometric components (sine and cosine waves). This method helps distinguish between market trends and random noise or price fluctuations. As a result, the LSTM network can identify patterns by focusing on the dominant frequency components, leading to more accurate forecasts.

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/Fourier%20Transforms.png)

**Autoregressive Integrated Moving Average (ARIMA)**: ARIMA models are employed to understand and forecast future price movements based on past values and trends within the time series data. By modeling the stock price as a combination of its previous values and moving averages of past errors, ARIMA helps capture the underlying patterns in the stock prices.

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/ARIMA%20autocorrelation.png)

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/ARIMA.png)

# RESULTS

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/Epoch%2050.png)

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/Epoch%20100.png)

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/4dfda22666bd982e2916f08585fb00a52bebfda4/Epoch%20150.png)

The model achieved an RMSE (Root Mean Squared Error) of 0.0474 and an MAE (Mean Absolute Error) of 0.0370, indicating a relatively low error rate in predicting the stock prices of Apple Inc. (AAPL). The RMSE measures how much the predictions deviate from the actual values on average, while the MAE reflects the average magnitude of errors in the predictions.

![alt text](https://github.com/nickmvega/Stock-Price-Prediction-using-LSTM-Networks-and-Bayesian-Optimization/blob/22ab27ef12ef4a40afa6546dfd348ff1edeb7981/Apple%20Predictions.png)

# POTENTIAL IMPROVEMENTS

While the model has shown strong performance, there are a couple of potential improvements:

Incorporating Sentiment Analysis: Integrating sentiment analysis from news articles, social media, and other textual data sources could provide valuable insights into market sentiment. 

Adding more features: The model was trained on a dataset comprising 1,401 samples and 80 features. However, incorporating additional features could enhance the model's predictive accuracy by providing more comprehensive insights into the factors influencing stock price movements.

Regularization Techniques: Implementing advanced regularization techniques, such as dropout with varied rates or L2 regularization, might help prevent overfitting.

Hyperparameter Tuning Optimization: While Bayesian optimization was used in this project, exploring other optimization techniques might yield even better results by exploring different hyperparameter spaces.
