# 📦 Time Series Forecasting 

## Project Overview

This project performs a **time series trend and pattern analysis** on the Kaggle Superstore Sales dataset using Python. The goal is to uncover underlying sales trends, seasonal patterns, and statistical properties of monthly sales data across product categories and regions.

The analysis uses **pandas** for data manipulation and **statsmodels** for time series decomposition and stationarity testing.

### 🔍 What This Project Covers

- Monthly sales aggregation from transactional order data
- Trend smoothing using rolling mean and standard deviation
- Seasonal decomposition (trend + seasonal + residual components)
- Stationarity testing using the Augmented Dickey-Fuller (ADF) test
- Autocorrelation (ACF) and Partial Autocorrelation (PACF) analysis
- Category-level sales trends (Furniture, Office Supplies, Technology)
- Seasonality profiling and year-over-year comparison

---

## 📁 Repository Structure

```
time-series-superstore/
│
├── data/
│   └── Sample - Superstore.csv       # Dataset (see download instructions below)
│
├── time_series_analysis.py           # Main analysis script
└── README.md
```

---

## 📊 Dataset

**Source:** [Kaggle – Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

To download the dataset:
1. Visit the link above (free Kaggle account required)
2. Click **Download** and extract the ZIP file
3. Place `Sample - Superstore.csv` inside the `data/` folder

---

## ⚙️ Requirements

Install the required Python libraries:

```bash
pip install pandas statsmodels matplotlib
```

---

## ▶️ How to Run

```bash
python time_series_analysis.py
```

Make sure `Sample - Superstore.csv` is in the `data/` folder, or update the file path in the script accordingly.

---

## 📈 Results / Key Findings

### 1. Overall Sales Trend
Monthly sales show a clear **upward trend** over the years, indicating consistent business growth across the analysis period.

### 2. Seasonality
Sales consistently **peak toward the end of the year** (October–December), likely driven by holiday and end-of-year purchasing cycles. February and April tend to be the weakest months.

### 3. Seasonal Decomposition
The additive decomposition confirms a **strong seasonal component** recurring annually, alongside a steady positive trend. Residuals are relatively small, suggesting the trend and seasonal components explain most of the variance.

### 4. Stationarity
The raw sales series is **non-stationary** (ADF p-value > 0.05), meaning it has a trend component. After applying first-order differencing, the series becomes stationary — making it suitable for ARIMA-based forecasting.

### 5. Category Trends
- **Technology** generates the highest sales volume and shows the steepest growth.
- **Office Supplies** is the most consistent category with lower volatility.
- **Furniture** shows moderate growth with occasional spikes.

---

## 🛠️ Future Work

- Build a SARIMA or Facebook Prophet forecasting model
- Add region-level analysis
- Create an interactive dashboard using Plotly or Streamlit
