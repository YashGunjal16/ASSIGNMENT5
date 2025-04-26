🚀 Univariate Time Series Forecasting using LSTM
This repository contains the implementation of an LSTM-based model for forecasting future values in a univariate time series environment, specifically forecasting daily minimum temperatures. The project uses the famous Daily Minimum Temperatures dataset and applies deep learning techniques for time series forecasting.

📖 Overview
This project aims to:

Forecast future daily minimum temperatures using deep learning.

Implement a Standard LSTM model for univariate time series forecasting.

Evaluate model performance using RMSE and MAE metrics.

Visualize the actual vs. predicted values.

📚 Problem Statement
Objective:
Forecast future temperature values based on historical daily minimum temperature data.

Dataset:

Source: Daily Minimum Temperatures in Melbourne, Australia (via TensorFlow/Kaggle)

Key Attribute: Temp (Temperature in degrees Celsius)

Timeframe: 1981 to 1990

🗃️ Dataset
Attributes:

Date (Timestamp)

Temp (Daily minimum temperature)

Data Source:
Automatically fetched using TensorFlow utilities from this URL.

🛠️ Methodology
Data Exploration & Preprocessing:

Load and inspect the dataset.

Focus on the Temp column.

Handle missing values (if any).

Normalization:

Apply MinMaxScaler to normalize temperature values between 0 and 1.

Sequence Generation:

Create input-output sequences using a 30-day lookback window.

Reshape the input to fit the LSTM requirements: [samples, timesteps, features].

Model Development:

Build a Sequential LSTM model:

One LSTM layer with 50 units and tanh activation.

A Dense output layer with one neuron (for the next day's prediction).

Compile with Adam optimizer and MSE loss.

Training and Evaluation:

Split data into 80% training and 20% testing.

Train the model using early stopping for optimization.

Evaluate the model performance using RMSE and MAE.

Visualization:

Plot actual vs. predicted temperatures to visually assess the model’s forecasting ability.

📊 Visualizations
The project includes:

Raw Time Series Plot:
Shows the original daily minimum temperatures over time.

Prediction vs Actual Plot:
Displays how closely the model's forecasted values align with the true observed temperatures.

📈 Model Performance
Evaluated using the testing dataset:

Root Mean Squared Error (RMSE): [value will vary depending on training run]

Mean Absolute Error (MAE): [value will vary depending on training run]

These metrics demonstrate how accurately the model captures the temperature trend.

🔍 Insights
LSTM models are effective for capturing sequential patterns in weather data.

Normalization and proper windowing are key to improving model accuracy.

Training on sliding windows helps the model generalize well over time.

🎯 Conclusion
This project successfully demonstrates the power of Long Short-Term Memory (LSTM) networks for univariate time series forecasting.
It highlights key practices such as:

Careful data preprocessing,

Sliding window generation,

Sequential model design,

Proper evaluation and visualization.

This approach can be extended to other time series domains like stock prediction, energy consumption forecasting, and more!

🙏 Acknowledgements
Dataset Source: Daily Minimum Temperatures in Melbourne (via TensorFlow / Kaggle)

Techniques inspired by best practices for deep learning in time series forecasting.

