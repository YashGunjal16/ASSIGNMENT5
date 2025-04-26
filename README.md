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

Reshape the input to fit the LSTM input format: [samples, timesteps, features].

Model Development:
Build a Sequential LSTM model:

One LSTM layer with 50 units and tanh activation.

A Dense output layer with one neuron (for next-day prediction).

Compile using Adam optimizer and MSE loss function.

Training and Evaluation:
Split data into 80% training and 20% testing sets.

Train the model using early stopping for better generalization.

Evaluate model performance using RMSE and MAE metrics.

Visualization:
Plot actual vs. predicted temperatures to visually assess the model’s forecasting ability.

📊 Visualizations
This project includes:

Raw Time Series Plot:
Displays the original daily minimum temperatures over time.

Prediction vs Actual Plot:
Shows how closely the model's forecasted values align with the true observed temperatures.

📈 Model Performance
Evaluated using the testing dataset:

Root Mean Squared Error (RMSE): (Value varies depending on training run)

Mean Absolute Error (MAE): (Value varies depending on training run)

These metrics demonstrate the model's ability to accurately capture the underlying temperature trend.

🔍 Insights
LSTM models are effective in capturing sequential patterns in weather data.

Normalization and proper windowing are crucial for improving model performance.

Training on sliding windows allows the model to generalize better over time.

🎯 Conclusion
This project successfully demonstrates the power of Long Short-Term Memory (LSTM) networks for univariate time series forecasting.

Key highlights include:

Careful data preprocessing,

Sliding window generation,

Sequential model design,

Proper evaluation and visualization.

This approach can be extended to other time series domains like stock price prediction, energy consumption forecasting, and many more!

🙏 Acknowledgements
Dataset Source: Daily Minimum Temperatures in Melbourne (via TensorFlow / Kaggle)

Techniques: Inspired by best practices for deep learning-based time series forecasting.
