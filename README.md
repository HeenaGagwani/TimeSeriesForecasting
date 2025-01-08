# Electricity Demand Time Series Forecasting

## Project Overview
This project analyzes and forecasts electricity demand in Great Britain using time series data from the National Grid ESO. The dataset, available on [Kaggle](https://www.kaggle.com/datasets/albertovidalrod/electricity-consumption-uk-20092022/data), includes electricity consumption records from 2009 onward, updated 48 times per day (every 30 minutes). The data was aggregated to a daily frequency by taking the maximum consumption value per day.

### Goal
Forecast maximum daily electricity consumption using exploratory data analysis (EDA) and accurate time series models.

---

## Dataset
- **Source**: National Grid ESO
- **Frequency**: Half-hourly (converted to daily)
- **Time Range**: 2009–2024
- **Data Preprocessing**:
  - Aggregated to daily frequency (maximum consumption per day)
  - Interpolated missing data points for consistency

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Analyzed trends, seasonality, and outliers in the time series data.
- Interpolated missing data points for consistency.

### 2. Statistical Analysis
- **Classical Decomposition**: Separated time series into trend, seasonality, and residual components.
- **Pymannkendall Test**: Checked for monotonic trends.
- **Kruskal-Wallis Test**: Tested for seasonality.

### 3. Stationarity Analysis
- **ADF Test**: Assessed stationarity.
- **KPSS Test**: Confirmed stationarity results.
- **ACF and PACF Plots**: Analyzed autocorrelations to identify seasonality and lag patterns.

### 4. Time Series Forecasting
- Developed and compared models:
  - **ARIMA**: Autoregressive Integrated Moving Average
  - **SARIMA**: Seasonal ARIMA
- Best model: **SARIMA(2,0,5)(5,1,2,7)**
- Evaluation metric: **MAPE = 3.5%**

---

## Results
The SARIMA model achieved a **MAPE of 3.5%**, effectively capturing both seasonal and non-seasonal patterns in electricity demand.

---

## Technologies Used
- **Python**: Core programming language
- **Pandas**: Data preprocessing
- **NumPy**: Numerical operations
- **Matplotlib** and **Seaborn**: Data visualization
- **Statsmodels**: Time series analysis and modeling
- **Pymannkendall**: Trend analysis

---

## Future Work
- Incorporate external features (e.g., temperature, holidays, day type) for improved accuracy.
- Explore advanced models like **Prophet** or **LSTM** for forecasting.

---

## Conclusion
This project demonstrates a comprehensive approach to time series forecasting, from EDA to building robust SARIMA models. The achieved **MAPE of 3.5%** reflects the model's accuracy and reliability in predicting electricity demand.

---

## Contact
For any questions or collaboration, feel free to reach out!

--- 
