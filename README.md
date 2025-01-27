Project: Bitcoin Price Prediction Using LSTM (Long Short-Term Memory) Network
Overview:
This project focuses on predicting the future price of Bitcoin using historical price data and applying a Long Short-Term Memory (LSTM) network. The goal is to demonstrate how machine learning can be applied to financial data, specifically cryptocurrency, to create predictive models that can aid investors and enthusiasts in making informed decisions.

Technologies Used:
Python
TensorFlow/Keras for building the LSTM model
pandas and NumPy for data manipulation
Matplotlib for data visualization
requests for fetching data from CoinGecko API
scikit-learn for model evaluation
Data Source:
The historical Bitcoin price data was fetched using the CoinGecko API, which provides real-time and historical cryptocurrency price information. In this project, we used Bitcoin's daily closing price data for the past 365 days.

Problem Statement:
The goal of the project is to predict Bitcoin’s future price based on past market data. Cryptocurrency markets are highly volatile, and having predictive models can provide valuable insights for making short-term and long-term investment decisions.

Steps Taken:
Data Collection: The data was fetched using the CoinGecko API, which provides daily market charts for Bitcoin. The dataset contains historical prices (in USD) with timestamps.

Data Preprocessing: The data was cleaned, and the timestamp was converted into a readable date format. The closing prices were then normalized using MinMaxScaler to scale the values between 0 and 1, which is essential for the LSTM model to learn effectively.

Model Building: A Long Short-Term Memory (LSTM) model was used for the prediction task. LSTM is a type of recurrent neural network (RNN) designed to handle sequences of data and is widely used in time-series forecasting. The model architecture includes:

Two LSTM layers with 50 units each
A Dense layer as the output layer
Model Training: The data was split into training and test sets. The LSTM model was trained on the training data for 10 epochs, using the Adam optimizer and mean squared error loss function.

Prediction and Evaluation: After training the model, predictions were made on the test data. The predicted values were then inverse-scaled to match the original scale of Bitcoin prices. The model’s performance was evaluated using Mean Absolute Error (MAE), which measures the average absolute difference between the predicted and actual prices.

Visualization: The predicted and actual prices were visualized on a plot to assess the model's accuracy visually. The results were promising, showing the model’s ability to capture the price trends.

Results:
The model was able to predict Bitcoin prices with a Mean Absolute Error (MAE) of around $16,600, which, although not perfect, shows reasonable accuracy for forecasting prices.
The model successfully identified general trends, such as price increases or decreases, despite the volatile nature of cryptocurrency markets.
Future Improvements:
Incorporating more features: Additional features such as trading volume, market sentiment, or social media trends could enhance the model’s predictive power.
Hyperparameter tuning: Optimizing the hyperparameters of the LSTM model (e.g., number of units, batch size, and epochs) could improve its accuracy.
Advanced Models: Exploring other models such as GRU (Gated Recurrent Units) or even hybrid models combining LSTM and other machine learning techniques could further enhance performance.
Conclusion:
This project demonstrates the application of deep learning techniques, specifically LSTM networks, to time-series forecasting in the cryptocurrency domain. While the results show promise, there is room for improvement, and with further optimization, the model could provide more accurate price predictions for Bitcoin and other cryptocurrencies.
