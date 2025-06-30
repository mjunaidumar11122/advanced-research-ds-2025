# advanced-research-ds-2025
mjunaidumar11122/Forecasting-crude-oil-prices-using-ARIMA-and-Prophet-models-on-Yahoo-Finance-data-2020-2024-.-Final
# Crude Oil Price Forecasting Project (ARIMA & Prophet)

##  Course:
Advanced Research Topics in Data Science (7PAM2016-0509-2024)

##  Overview
This project explores the use of two powerful time series forecasting models — **ARIMA** and **Facebook Prophet** — to predict crude oil prices for the years 2023 and 2024. Historical data from **Yahoo Finance (2020–2022)** was used to train the models, and the results were validated against real-world data from 2023–2024.

The goal is to compare the predictive performance of ARIMA and Prophet in terms of:
- Trend and seasonality capture
- Short-term shock responsiveness
- Forecast accuracy and limitations

---

##  Project Structure

- `FR_USAMA_01.ipynb` — Main notebook including:
  - Data preprocessing and transformation
  - ADF tests and differencing
  - ARIMA modeling and diagnostics
  - Prophet modeling and seasonal decomposition
  - Forecast results vs actual 2023–2024 data

- `arima_forecast.png`, `prophet_forecast.png` — Visualizations comparing model predictions to actual prices.

- `README.md` — This file, containing the project overview, methodology, and findings.

---

##  Dataset

- **Source**: Yahoo Finance  
- **Period**: July 2020 – December 2022 (training), Jan 2023 – Dec 2024 (validation)  
- **Features**:
  - Date
  - Daily closing price of crude oil (USD)

---

##  Models Used

| Model           | Description |
|------------------|-------------|
| ARIMA (2,1,2)    | Statistical time series model suitable for stationary data with autocorrelation |
| Facebook Prophet | Additive model capable of detecting seasonality, holidays, and changepoints |

---

##  Methodology

- **Stationarity Check**: Augmented Dickey-Fuller (ADF) test  
- **Differencing**: First-order differencing to stabilize mean  
- **Model Selection**: AIC-based grid search for best ARIMA parameters  
- **Seasonality Decomposition**: Prophet model used to extract trend, weekly and yearly components  
- **Validation**:
  - Actual oil prices (2023–2024) from Yahoo Finance
  - Forecasts vs Actual: Visual and statistical comparison

---

##  Results

- **ARIMA** showed good performance on historical data but failed to respond to unpredictable real-world shocks and over-smoothed the forecast.
- **Prophet** captured seasonality well but **underestimated oil prices**, especially in late 2024.
- Both models showed limitations in anticipating external macroeconomic or geopolitical events.

---

##  Technologies Used

- Python 3.11  
- Google Colab  
- `statsmodels` (for ARIMA)  
- `fbprophet` / `prophet`  
- `matplotlib`, `seaborn`  
- Yahoo Finance historical data

---

##  Ethical Considerations

- All data used is **publicly available** and **anonymized**.
- No proprietary or sensitive financial information was used.
- The project complies with ethical research and data usage standards.

---

##  Future Work

- Integrate **exogenous variables** (e.g., inflation, geopolitical indices)
- Experiment with **SARIMA** and **ARIMAX** extensions
- Build **hybrid models** combining Prophet with machine learning (e.g., LSTM)
- Deploy real-time API or dashboard for rolling forecasts

---

##  Acknowledgment

Special thanks to Yahoo Finance for providing accessible historical oil price data and to the faculty and mentors of *Advanced Research Topics in Data Science* for their support and guidance throughout this project.
