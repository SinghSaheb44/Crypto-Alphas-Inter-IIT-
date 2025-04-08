# 📈 Inter IIT 13.0 - Untrade Crypto Trading Challenge

## 🚀 Project Overview

This repository contains the **algorithmic trading strategies** developed by **Team 53** for the **Inter IIT 13.0 Tech Meet - Untrade Crypto Trading Challenge**. The project focuses on designing and implementing robust trading strategies for the highly volatile **BTC/USDT** and **ETH/USDT** cryptocurrency markets.

These strategies leverage a combination of:
- **Technical indicators**
- **Machine learning models**
- **Advanced statistical methods**

All with the aim to **maximize returns while managing risk**.

---

## 🔑 Key Features

- **Multiple Trading Strategies**: Four distinct strategies tailored for different timeframes and market conditions.
- **Technical Indicators**: Utilizes RSI, MACD, Bollinger Bands, ATR, EMA, VWAP, and more.
- **Advanced Techniques**: Incorporates Hawkes Process, Fibonacci retracements, and ML models (PatchTST, XGBoost, ARIMA-LSTM).
- **Risk Management**: Dynamic stop-loss mechanisms, volatility filters, and asymmetric risk controls.
- **Performance Metrics**: Detailed backtesting results, including **Sharpe Ratio**, **Sortino Ratio**, and **annualized returns**.

---

## 🧠 Strategies

### 1. **Volume and Volatility-Driven EMA with RSI Confirmation** *(BTC-USDT-15M)*

- **Components**: RSI, EMA, VWAP, ADX, ATR, Bollinger Bands, Heikin Ashi, Volume SMA  
- **Hypothesis**: Combines momentum and volatility indicators to identify high-probability trades.

**Performance:**
- 📈 **Return**: 8938% (2020–2023)
- 📊 **Sharpe Ratio**: 4.415
- 🎯 **Win Rate**: 37.29%

---

### 2. **Hawkes Process with Fibonacci Exit** *(BTC-USDT-4H)*

- **Components**: Hawkes Intensity Function, ADX, Bollinger Bands, Fibonacci Retracements  
- **Hypothesis**: Uses self-exciting point processes to detect high-impact market conditions.

**Performance:**
- 📈 **Return**: 1706% (1x Leverage), 8814% (2x Leverage)
- 📊 **Sharpe Ratio**: 3.792
- 🎯 **Win Rate**: 64.81%

---

### 3. **Hawkes-Driven Multi-Indicator Strategy** *(ETH-USDT-4H)*

- **Components**: Heikin Ashi, ATR, Hawkes Process, ADX, RSI, MACD, Bollinger Bands  
- **Hypothesis**: Balances trend-following and reversal signals with dynamic exits.

**Performance:**
- 📈 **Return**: 2265% (1x Leverage), 22789% (2x Leverage)
- 📊 **Sharpe Ratio**: 5.399
- 🎯 **Win Rate**: 52.38%

---

### 4. **MACD with EMA Crossover** *(ETH-USDT-30M)*

- **Components**: Heikin Ashi, EMA, MACD, Parabolic SAR, ATR, RSI, VWAP  
- **Hypothesis**: Combines trend confirmation with momentum shifts for precise entries/exits.

**Performance:**
- 📈 **Return**: 4204%
- 📊 **Sharpe Ratio**: 5.646
- 🎯 **Win Rate**: 44.12%

---

## 🤖 Machine Learning Approaches

### 🔹 PatchTST (Time Series Transformer)
- **Description**: Predicts future prices, SMAs, and EMAs using transformer-based models.
- **Metrics**:
  - MSE: `5249.45`
  - MAPE: `6.93%`

---

### 🔹 XGBoost
- **Description**: Uses oscillator-based indicators for trade predictions, validated with moving average crossovers.
- **Metrics**:
  - Return: `9.5%`
  - Sharpe Ratio: `2.653`

---

### 🔹 ARIMA-LSTM
- **Description**: Hybrid model combining LSTM (deep learning) and ARIMA (statistical) for price forecasting.
- **Metrics**:
  - Return: `59.3%`
  - Sharpe Ratio: `2.475`

---

## ⚠️ Challenges Faced

- **Market Complexity**: High volatility and lack of long-term historical data.
- **Timeframe Optimization**: Unique parameter tuning required for each timeframe.
- **Overfitting Risks**: Ensuring strategies generalize well to unseen data.
- **Advanced Concepts**: Learning and integrating techniques like the Hawkes Process.

---

## 🔮 Future Improvements

- **BTC-ETH Pairs Trading**: Exploring cointegration-based strategies despite initial challenges.
- **Sentiment Analysis**: Incorporating Fear and Greed Index for signal validation.
- **On-Chain Data**: Utilizing metrics like hash ribbon index for miner sentiment.

---

## 📁 Repository Structure

├── Strategies/                # Code for each trading strategy
│   ├── Strategy_1/            # Volume and Volatility-Driven EMA
│   ├── Strategy_2/            # Hawkes Process with Fibonacci
│   ├── Strategy_3/            # Hawkes Multi-Indicator
│   └── Strategy_4/            # MACD with EMA Crossover
├── ML_Models/                 # Machine learning models
│   ├── PatchTST/              # Transformer-based forecasting
│   ├── XGBoost/               # Classifier for trade signals
│   └── ARIMA_LSTM/            # Hybrid forecasting model
├── Data/                      # Historical price and indicator data
├── Results/                   # Backtesting performance metrics
├── Docs/                      # Project report and documentation
└── README.md                  # This file

---

## 👥 Contributors

```text
Team 53, Inter IIT 13.0 Tech Meet



