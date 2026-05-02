# walmart-sales-forecasting
Time series forecasting of Walmart weekly sales using ARIMA and Prophet | Python, statsmodels, Prophet, scikit-learn

# Walmart Sales Forecasting

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![Time Series](https://img.shields.io/badge/Topic-Time%20Series-green) ![ARIMA](https://img.shields.io/badge/Model-ARIMA-purple) ![Prophet](https://img.shields.io/badge/Model-Prophet-orange)

End-to-end time series forecasting project using Walmart's weekly sales data. Covers data loading from Kaggle, seasonal decomposition, ARIMA and Prophet modelling, and business insight generation.

## Overview

This project forecasts total weekly sales across all Walmart stores and departments using two models — ARIMA and Facebook Prophet — and compares their performance on a held-out 2012 test set.

## Dataset

Source: `aslanahmedov/walmart-sales-forecast` on Kaggle (loaded via `kagglehub`).

- Date range: February 2010 – October 2012
- 45 stores, multiple departments
- Key column: `Weekly_Sales`

## Project Steps

1. Import libraries
2. Load dataset via kagglehub
3. Data exploration & preprocessing
4. Aggregate to total weekly sales
5. Time series visualization
6. Seasonal decomposition (period=52)
7. Train-test split — train: 2010–2011, test: 2012
8. ARIMA(1,1,1) model
9. ARIMA forecast
10. Plot ARIMA results
11. Evaluate ARIMA — MAE, RMSE, MAPE
12. Prophet model setup
13. Prophet forecast & components plot
14. Evaluate Prophet
15. Model comparison
16. Business insights

## Installation

```bash
git clone https://github.com/your-username/walmart-sales-forecasting.git
cd walmart-sales-forecasting
pip install -r requirements.txt
```

### requirements.txt

```
pandas
numpy
matplotlib
seaborn
statsmodels
scikit-learn
prophet
kagglehub
```

## Usage

```bash
jupyter notebook walmart_sales_forecasting.ipynb
```

Make sure your Kaggle API credentials are configured before running (`~/.kaggle/kaggle.json`).

## Results

- Sales show clear yearly seasonality with peaks in Nov–Dec (holidays)
- An upward trend is visible from 2010 to 2012
- Prophet outperforms ARIMA due to better handling of seasonality and trend shifts

## File Structure

```
walmart-sales-forecasting/
├── walmart_sales_forecasting.ipynb
├── requirements.txt
└── README.md
```

---
Dataset credit: Kaggle — aslanahmedov/walmart-sales-forecast
