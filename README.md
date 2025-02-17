# Time Series Analysis and Forecasting of Yield Curves

## Overview
This project analyzes and forecasts yield curve data, focusing on interest rates for bonds with maturities ranging from 3 months to 30 years. Data spanning 2020 through 2024 is used to perform an end-to-end analysis—from data extraction and exploratory data analysis (EDA) to stationarity testing and time series forecasting using exponential smoothing and ARIMA/SARIMA models.

## Data Sources
- [FRED - Interest Rate Series](https://fred.stlouisfed.org/series/IR3TTS01CNM156N)
- [CBIRC - National Debt and Other Bond Yields](https://www.cbirc.gov.cn/cn/view/pages/index/guozhai.html)

## Data Extraction and Preprocessing
- **Data Loading:** Excel files for each year (2020 to 2024) are loaded and concatenated into a single DataFrame.
- **Preprocessing Steps:**
  - Converting date columns to datetime objects.
  - Setting the date as the DataFrame index.
  - Sorting data chronologically.
  - Dropping unnecessary columns and handling missing dates.

## Exploratory Data Analysis (EDA)
- **Summary Statistics:** Generates summary statistics and boxplots to understand the distribution.
- **Visualizations:** 
  - 3D surface plots and wireframe plots to visualize the evolution of yield curves.
  - Yearly average yield curves and time series plots for interest rates.
- **Correlation Analysis:** Examines correlations between yields of different maturities.

## Stationarity Testing
- **Augmented Dickey-Fuller (ADF) Tests:** Conducted on the original, first-differenced, and seasonally differenced series to check for stationarity and determine the need for differencing.

## Time Series Forecasting Models
- **Exponential Smoothing (ETS):** Both additive and multiplicative models are applied.
- **ARIMA Modeling:** An ARIMA model (e.g., ARIMA(1,1,2)) is fitted to the data.
- **SARIMA Modeling:** A grid search is performed over parameter combinations to find the best seasonal ARIMA model based on the Akaike Information Criterion (AIC).

## Model Evaluation
- **Data Split:** 
  - Training set: 2020 to end of 2023.
  - Testing set: 2024.
- **Evaluation Metrics:** Uses Mean Squared Error (MSE) and Mean Absolute Error (MAE) to assess model performance.

## Installation and Dependencies
Ensure you have the following Python libraries installed:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `statsmodels`
- `pmdarima`
- `scikit-learn`
- `openpyxl` (for reading Excel files)

Install the dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn statsmodels pmdarima scikit-learn openpyxl
