Time Series Analysis and Forecasting of Yield Curves
Overview
This project analyzes and forecasts yield curve data, focusing on interest rates for bonds with maturities ranging from 3 months to 30 years. Data spanning 2020 through 2024 is used to perform an end-to-end analysis—from data extraction and exploratory data analysis (EDA) to stationarity testing and time series forecasting using exponential smoothing and ARIMA/SARIMA models. 

Data Sources
FRED - Interest Rate Series
CBIRC - National Debt and Other Bond Yields

Data Extraction and Preprocessing
The project reads annual yield curve data from Excel files for the years 2020 through 2024. Key preprocessing steps include:
Loading each year's data and concatenating them into a single DataFrame.
Converting date columns into datetime objects and setting the date as the DataFrame index.
Sorting the data chronologically and dropping unnecessary columns.
Identifying and handling missing dates. 
Exploratory Data Analysis (EDA)

The analysis includes:
Generating summary statistics and visualizing distributions with boxplots.
Creating 3D surface plots and wireframe plots to visualize the evolution of yield curves over trading months.
Plotting yearly average yield curves and interest rate time series.
Conducting correlation analysis between yields of different maturities. 
Stationarity Testing
To determine the appropriate modeling approach, the project tests the stationarity of the time series using the Augmented Dickey-Fuller (ADF) test. Tests are performed on:

The original series.
The first-differenced series.
The seasonally differenced series. These tests help in understanding trends, seasonality, and the need for differencing prior to modeling. 

Time Series Forecasting Models
Forecasting is carried out using several approaches:

Exponential Smoothing (ETS):
Both additive and multiplicative models are implemented to capture trend and seasonal components.
ARIMA Modeling:
A manual ARIMA model (e.g., ARIMA(1,1,2)) is fitted to the data, with forecast results compared against other models.
SARIMA Modeling:
A grid search over possible parameter combinations is performed to identify the best seasonal ARIMA model based on the Akaike Information Criterion (AIC). 
Model Evaluation
The dataset is split into training and testing sets:

Training Set: Data from 2020 to the end of 2023.
Testing Set: Data for 2024. Evaluation metrics such as Mean Squared Error (MSE) and Mean Absolute Error (MAE) are used to assess model performance.
