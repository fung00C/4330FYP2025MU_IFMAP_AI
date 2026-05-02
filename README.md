# FYP - S&P 500 Index and Component Stocks Price Prediction

A Final Year Project using **LSTM** deep learning models to predict the prices of the S&P 500 index and its 487 component stocks.

---

## 📋 Project Overview

This project is divided into two main parts:

- **SP500 Model**: Training a single LSTM model to predict the future price of the S&P 500 index.
- **Stocks Models**: Training individual LSTM models for each of the **487 component stocks** of the S&P 500 index.

Both Notebooks include the complete pipeline: data collection, preprocessing, feature engineering, model training, evaluation, and visualization.

---

## ✨ Key Features

- Automatically download historical stock price data from 2008 to 2025 using yfinance.
- Calculate various Technical Indicators using TA-Lib.
- Time series data processing (Sliding Window).
- Data normalization (MinMaxScaler).
- LSTM model construction and training (including Dropout to prevent overfitting).
- Model evaluation (RMSE, MSE, MAE).
- Visualization of actual vs. predicted price trends.
- Batch training and automatic saving of all stock models.

---

## 🛠 Tech Stack

- **Programming Language**: Python 3.11
- **Data Retrieval**: yfinance
- **Technical Indicators**: TA-Lib
- **Data Processing**: pandas, numpy
- **Deep Learning**: Keras / TensorFlow (LSTM)
- **Visualization**: matplotlib
- **Environment**: Google Colab (GPU Acceleration)

---

## 📁 Project Directory Structure

```bash
/
├── sp500_model_training.ipynb          # Main program for S&P 500 index model training
├── stocks_model_training.ipynb         # Main program for 487 component stocks model training
├── stock_category.json                 # S&P 500 component stocks classification data
├── models/                             # Directory for storing trained models
│   ├── SP500_model.h5
│   └── AAPL_model.h5
│   └── ...
├── input/                              # (Optional) Original CSV folder
└── README.md
/
```

## 🚀 Installation & Execution
1. Install dependencies
```bash
pip install yfinance pandas numpy matplotlib tensorflow keras scikit-learn
```
  - TA-Lib Installation (Colab environment)
  - The installation commands are already included in the Notebook, just run them directly.
2. Execution steps

## 🔧 Model Architecture

- Multi-layer LSTM + Dropout
- Huber Loss with Adam Optimizer
- Time series sliding window input
- Single-step prediction (can be extended to multi-step prediction)


## 📈 Future Optimization Directions

- Incorporate macroeconomic indicators and market sentiment analysis
- Utilize Transformer or Temporal Fusion Transformer models
- Ensemble Learning
- Combine with trading strategies for backtesting
- Real-time prediction system development
