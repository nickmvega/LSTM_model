# INTRODUCTION

This project uses a comprehensive data-driven approach to predict Apple Inc. (AAPL) stock price movements. The model is built on a robust feature set incorporating correlated assets, technical indicators, Fourier transforms, and ARIMA models, all processed and visualized using pandas and matplotlib.

The model's core is a Long Short-Term Memory (LSTM) network designed explicitly for time-series forecasting. Through Bayesian optimization, the hyperparameters of the LSTM model are fine-tuned to improve accuracy and performance, enabling the model to effectively capture temporal dependencies and market patterns in an increasingly complex financial landscape.

The entire pipeline is in Stock_Prediction_Model.ipynb

# RESULTS

The model achieved an RMSE (Root Mean Squared Error) of 0.0474 and an MAE (Mean Absolute Error) of 0.0370, indicating a relatively low error rate in predicting the stock prices of Apple Inc. (AAPL). The RMSE measures how much the predictions deviate from the actual values on average, while the MAE reflects the average magnitude of errors in the predictions.

A visual of the predictions can be seen in Apple Predictions.png.

# POTENTIAL IMPROVEMENTS

While the model has shown strong performance, there are a couple of potential improvements:

Incorporating Sentiment Analysis: Integrating sentiment analysis from news articles, social media, and other textual data sources could provide valuable insights into market sentiment. 

Adding more features: The model was trained on a dataset comprising 1,401 samples and 80 features. However, incorporating additional features could enhance the model's predictive accuracy by providing more comprehensive insights into the factors influencing stock price movements.

Regularization Techniques: Implementing advanced regularization techniques, such as dropout with varied rates or L2 regularization, might help prevent overfitting.

Hyperparameter Tuning Optimization: While Bayesian optimization was used in this project, exploring other optimization techniques might yield even better results by exploring different hyperparameter spaces.
