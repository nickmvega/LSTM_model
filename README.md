# INTRODUCTION

This project uses a comprehensive data-driven approach to predict Apple Inc. (AAPL) stock price movements. The model is built on a robust feature set incorporating correlated assets, technical indicators, Fourier transforms, and ARIMA models, all processed and visualized using pandas and matplotlib.

The model's core is a Long Short-Term Memory (LSTM) network designed explicitly for time-series forecasting. Through Bayesian optimization, the hyperparameters of the LSTM model are fine-tuned to improve accuracy and performance, enabling the model to effectively capture temporal dependencies and market patterns in an increasingly complex financial landscape.

The entire pipeline is in Stock_Prediction_Model.ipynb

# THE DATA

To predict AAPL stock price movements, a substantial amount of data and a variety of features are essential. In this project, the dataset consisted of 2,429 days, with 1,700 days allocated for training and 729 days for testing.

Correlated Assets: The AAPL stock price is influenced by the performance of correlated assets, such as other technology companies, indices, and related sectors. These assets provide additional context by reflecting market conditions, sector trends, and external factors that may impact AAPL's stock price. For example, the performance of Amazon or Microsoft can indicate broader industry movements that AAPL might follow, making these correlations valuable predictors.

Technical Indicators: Various technical indicators were employed to capture different aspects of the stock's price behavior:

Simple Moving Averages (SMA): The 7-day and 21-day SMAs smooth out short-term price fluctuations, helping to identify the overall trend direction.

Exponential Moving Averages (EMA): The 12-day and 26-day EMAs give more weight to recent prices, making them more responsive to new information and helpful in detecting short-term momentum changes.

MACD and Signal Line: The Moving Average Convergence Divergence (MACD) and its Signal Line are crucial for identifying changes in a trend's strength, direction, momentum, and duration.

Relative Strength Index (RSI): The 14-day RSI measures the speed and change of price movements, helping to identify overbought or oversold conditions that could indicate potential reversals.

Bollinger Bands: These bands measure volatility by placing standard deviation lines above and below a moving average, identifying overextended price moves that may revert to the mean.

Momentum: This indicator captures the rate of price change, which is essential for understanding the stock's acceleration or deceleration over time.

Fourier Transforms: Beyond the daily closing price, Fourier transforms were utilized to extract underlying trends by breaking the price series into its sinusoidal components. This method helps distinguish between market trends and random noise or price fluctations. The LSTM network can better identify patterns by focusing on the dominant frequency components, leading to more accurate forecasts.

Autoregressive Integrated Moving Average (ARIMA): ARIMA models are employed to understand and forecast future price movements based on past values and trends within the time series data. By modeling the stock price as a combination of its previous values (autoregression) and moving averages of past errors, ARIMA helps capture the underlying patterns and cyclical behaviors in the stock prices, making it a vital component in the prediction framework.

# RESULTS

The model achieved an RMSE (Root Mean Squared Error) of 0.0474 and an MAE (Mean Absolute Error) of 0.0370, indicating a relatively low error rate in predicting the stock prices of Apple Inc. (AAPL). The RMSE measures how much the predictions deviate from the actual values on average, while the MAE reflects the average magnitude of errors in the predictions.

![Alt text](/Apple Predictions.png)

# POTENTIAL IMPROVEMENTS

While the model has shown strong performance, there are a couple of potential improvements:

Incorporating Sentiment Analysis: Integrating sentiment analysis from news articles, social media, and other textual data sources could provide valuable insights into market sentiment. 

Adding more features: The model was trained on a dataset comprising 1,401 samples and 80 features. However, incorporating additional features could enhance the model's predictive accuracy by providing more comprehensive insights into the factors influencing stock price movements.

Regularization Techniques: Implementing advanced regularization techniques, such as dropout with varied rates or L2 regularization, might help prevent overfitting.

Hyperparameter Tuning Optimization: While Bayesian optimization was used in this project, exploring other optimization techniques might yield even better results by exploring different hyperparameter spaces.
