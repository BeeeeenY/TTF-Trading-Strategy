# TTF Price Forecasting and Spread Trading Strategy
Machine Learning Enhanced Trading Strategies for TTF (Title Transfer Facility) Natural Gas Markets

## Overview

This repository consists of two main components:

1. **`ML_price_regression.ipynb`**  
   This notebook performs machine learning-based forecasting for the Title Transfer Facility (TTF) natural gas front-month price using both LSTM and XGBoost regression models. It also includes exploratory analysis using correlation and cointegration tests between TTF and key related variables (Brent crude and Carbon prices).

2. **`SpreadTrade.ipynb`**  
   This notebook implements a spread trading strategy that leverages the predictions generated from the ML model. It builds on top of the forecasted price data to construct and evaluate a spread trading portfolio.

## Folder Structure

```bash
├── ML_price_regression.ipynb             # ML model training and forecast (LSTM & XGBoost)
├── SpreadTrade.ipynb                 # Spread trading strategy using forecasted data
├── master_noNA.xlsx                      # Original cleaned dataset (input to ML notebook)
├── master_with_lstm_and_xgb_preds.xlsx   # Output from ML notebook, used in trading notebook
├── README.md                             # Project documentation
```

## Workflow Summary

### 📈 ML_price_regression.ipynb

- **Input**: `master_noNA.xlsx`
- **Processes**:
  - Data preprocessing (feature engineering, scaling, etc.)
  - LSTM model training
  - XGBoost model training
  - Correlation analysis (e.g., TTF vs Brent, TTF vs EUA)
  - Cointegration testing using Engle-Granger method
- **Output**: `master_with_lstm_and_xgb_preds.xlsx`

### 💹 SpreadTrade.ipynb

- **Input**: `master_with_lstm_and_xgb_preds.xlsx`
- **Processes**:
  - Load predicted price series
  - Construct and evaluate spread trading positions
  - Evaluate PnL and risk metrics for strategy performance

## Key Dependencies

- Python 3.x
- pandas
- numpy
- scikit-learn
- statsmodels
- xgboost
- tensorflow / keras
- matplotlib / seaborn

## Usage

1. Run `ML_price_regression.ipynb` to:
   - Train LSTM and XGBoost models
   - Generate predicted TTF prices
   - Perform correlation and cointegration analysis

2. Run `SpreadTrade.ipynb` to:
   - Execute and backtest the spread trading strategy
   - Visualize strategy results and evaluate trading performance


## Author

Yin Qiuhao  
Singapore Management University  
Email: qiuhao.yin.2022@scis.smu.edu.sg  
[LinkedIn](https://www.linkedin.com/in/qiuhaoyin)
