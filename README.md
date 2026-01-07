# Chronos-trade-Wids-2025-
# Assignment 1  
## Time-Series Stock Price Forecasting Using ARIMA and LSTM Models


---

## 1. Data Collection

Stock price data for the last 5 years is downloaded using the `yfinance` library.  
The dataset is cleaned by removing unused features and checking for missing values.

---

## 2. Data Normalization

A MinMaxScaler is used to scale the data between 0 and 1.  
The normalized close prices are used for deep learning models.

---

## 3. Stationarity Analysis

- Rolling mean and standard deviation (window = 12)
- ACF and PACF plots  
These diagnostics guide ARIMA parameter selection and confirm stationarity after differencing.

---

## 4. ARIMA Modeling

A grid search is run to determine the best `(p, d, q)` order.  
Residual analysis and forecast visualization are included.  
Testing performance is compared against actual values.

---

## 5. Deep Learning Models

Sequences are created using a sliding window approach.

Models trained:

- LSTM  
- LSTM with Dropout  
- Bidirectional LSTM  

Training involves 50 epochs, Adam optimizer, and MSE loss.  
Actual vs predicted plots are generated for all models.

---

## 6. Model Evaluation

Metrics computed:

- MAE  
- MSE  
- RMSE  

Comparison across ARIMA, LSTM, Dropout-LSTM, and Bidirectional LSTM.

---

## 7. Learning Curves

Training and validation loss curves are plotted for deep learning models to analyze overfitting or underfitting.

---

# Assignment 2  
## Forecasting Stock Prices for the Last Five Years (Specific Ticker)

This assignment focuses on forecasting stock prices of a specific ticker (such as a large technology company) over the last five years.

---

## 1. Data Collection

- Historical stock data of the selected company is downloaded using `yfinance`.
- Data includes Open, High, Low, Close, Adj Close, and Volume.
- Only the Close price is used for forecasting.

---

## 2. Data Cleaning

- Missing values removed  
- Date index verified  
- Dataset filtered to ensure 5-year time span  

---

## 3. Train-Test Split

- 80% training data  
- 20% testing data  

Visualizations include full-series plotting and train-test separation.

---

## 4. ARIMA Forecasting

- Differencing applied to make data stationary  
- ACF/PACF used to identify approximate ARIMA order  
- ARIMA model fitted on training data  
- Predictions compared with actual test values  

Residual analysis is also performed.

---

## 5. LSTM Forecasting

- Data normalized using MinMaxScaler  
- Windowed sequences created  
- LSTM model built using Keras  
- Training performed for 50 epochs  

Outputs include:

- Training and validation loss curves  
- Actual vs Predicted test values  

---

## 6. Final Comparison

Metrics calculated:

- MAE  
- MSE  
- RMSE  

The final section compares ARIMA and LSTM performance and provides observations about which model performs better for this dataset.

---


```


