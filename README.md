# Time Series Analysis

This project focuses on predicting stock prices using various statistical and deep learning models, including ARIMA, GRU, LSTM, and RNN. Stock data is sourced from Yahoo Finance using the `yfinance` library, specifically utilizing daily stock price data.

## Data Description

The dataset comprises daily stock prices, including:
- Open Price
- High Price
- Low Price
- Close Price
- Volume

The closing prices are primarily used to train and test the models. Data is fetched via the `yfinance` library.

## Techniques and Models

### 1. ARIMA (AutoRegressive Integrated Moving Average)

- **Stationarity Test**: I applied the Dickey-Fuller Test to verify if the time series data was stationary. Non-stationary data was made stationary using first-order differencing.
- **Model Selection**: Based on autocorrelation and partial autocorrelation plots, I identified the optimal parameters for the ARIMA model.
- **ARIMA Model**: An ARIMA(1,1,1) model was used for stock price forecasting.

### 2. Deep Learning Models (GRU, LSTM, and RNN)

The following steps were followed for all deep learning models:
- **Data Preparation**: I split the closing prices into training and test sets, and scaled the data using normalization techniques.
- **Modeling**: Applied the deep learning models (GRU, LSTM, and RNN) to predict stock prices.

## Results

- The **LSTM** model yielded the best performance with a **Mean Squared Error (MSE)** of `6.41` and an **R-squared (R2) value** of `0.94`. 
- This suggests that LSTM is highly effective at capturing long-term dependencies in time series stock data.

## Conclusion

The project demonstrates the effectiveness of deep learning models, especially LSTM, for predicting stock prices. The model can be further applied to forecast other stocks and generate potentially profitable insights.

## How to Run the Project

### Prerequisites
- Python 3.x
- `yfinance` library
- `numpy`, `pandas`, `matplotlib`
- `statsmodels` (for ARIMA)
- `tensorflow` (for deep learning models)
