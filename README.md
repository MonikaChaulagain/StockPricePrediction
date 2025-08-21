# 📈 Stock Price Prediction with LSTM

This project implements a Long Short-Term Memory (LSTM) neural network in PyTorch to predict stock prices based on historical time series data. It demonstrates the full workflow: preprocessing, sequence generation, model training with early stopping, and evaluation on unseen data.

##  Features

* Preprocessing with **MinMax scaling** for both features and target.
* Creation of input sequences (`X`) and target values (`y`) for supervised learning.
* **PyTorch LSTM model** with dropout and fully connected output layer.
* **Early stopping** to prevent overfitting.
* Evaluation using MSE.
* Visualization of **Predicted vs Actual** stock prices.


## 📊 Data Preparation

1. Collect stock price data (e.g., from Yahoo Finance).
2. Place the CSV in the `data/` folder.
3. Preprocess with:

   * **MinMaxScaler** → scale both features and target between 0–1.
   * **Sequence generator** → convert time series into `(X, y)` pairs. Example with `seq_length=10`:

     * Input: prices from `t-10 ... t-1`
     * Target: price at `t`


## 🧠 Model Architecture

* **LSTM Layer(s)** → capture temporal dependencies.
* **Dropout Layer** → reduce overfitting.
* **Fully Connected (Linear) Layer** → predict next price.


## 🔮 Results

* Model captures **overall trend** well.
* Predictions are smoother than actuals (underestimate volatility).
* Performance improves with more features (volume, technical indicators).

