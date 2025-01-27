# Bitcoin Price Prediction Using LSTM Network

This project demonstrates the use of a Long Short-Term Memory (LSTM) network to predict the future price of Bitcoin based on historical price data. By leveraging deep learning, this model aims to capture the trends and patterns in the volatile cryptocurrency market and make future price predictions.

## Technologies Used:
- **Python**
- **TensorFlow** / **Keras** for building the LSTM model
- **pandas** and **NumPy** for data manipulation
- **Matplotlib** for data visualization
- **requests** for fetching data from the CoinGecko API
- **scikit-learn** for data preprocessing and model evaluation

## Data Source:
The historical Bitcoin price data was fetched from the [CoinGecko API](https://www.coingecko.com/). This API provides real-time and historical cryptocurrency data, and in this project, Bitcoin’s daily closing price data for the last 365 days was used.

## Project Workflow:
1. **Data Collection**:
   - Fetch Bitcoin’s historical daily price data from the CoinGecko API.
   - Convert timestamps to readable dates and format the data into a pandas DataFrame.

2. **Data Preprocessing**:
   - Normalize the price data using **MinMaxScaler** to scale the values between 0 and 1.
   - Split the data into training and test sets.

3. **Model Development**:
   - Built an LSTM (Long Short-Term Memory) network to predict future Bitcoin prices.
   - The LSTM model consists of two LSTM layers and a Dense output layer.

4. **Model Training**:
   - The model was trained using the training dataset with 10 epochs and Adam optimizer.
   
5. **Prediction and Evaluation**:
   - The model made predictions on the test set, which were inverse-scaled back to their original values.
   - Evaluated the model’s performance using **Mean Absolute Error (MAE)**.

6. **Results Visualization**:
   - Visualized both actual and predicted prices to assess the accuracy of the model.

## Results:
- The LSTM model was able to predict Bitcoin’s price with a **Mean Absolute Error (MAE)** of **$16,600**, capturing the general trends of price movement.
- The model can predict future Bitcoin prices and trends but can be improved with further adjustments.

## Future Improvements:
- Incorporating additional features like trading volume, market sentiment, or social media data could improve the model's accuracy.
- Hyperparameter tuning to optimize the model’s performance (e.g., changing the number of LSTM units, batch size, epochs).
- Experimenting with other models like **GRU (Gated Recurrent Units)** or hybrid models to further enhance the results.

## Running the Project:
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/md-abdulaziz/bitcoin_price_detection.git
2. Install the required dependencies:
   pip install -r requirements.txt
3. Run the script to fetch data, train the model, and evaluate predictions:
   bitcoin_price_prediction.ipynb
License:
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements:
Thanks to the CoinGecko API for providing the historical cryptocurrency data.
Thanks to TensorFlow and Keras for the powerful deep learning frameworks used in the project.


