# A Yen For The Future

## Background

The financial departments of large companies often deal with foreign currency transactions while doing international business. As a result, they are always looking for anything that can help them better understand the future direction and risk of various currencies. Hedge funds, too, are keenly interested in anything that will give them a consistent edge in predicting currency movements.
In this Analysis, I will test my data using the ARMA, ARIMA, and GARCH models in order to predict future movements in the value of the Japanese yen versus the U.S. dollar.

### Instructions

#### Time-Series Forecasting

In this notebook, you will load historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

Follow the steps outlined in the time-series starter notebook to complete the following:

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

Use the results of the time series analysis and modeling to answer the following questions:

1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?


#### Linear Regression Forecasting

In this notebook, you will build a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

Follow the steps outlined in the regression_analysis starter notebook to complete the following:

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

Use the results of the linear regression analysis and modeling to answer the following question:

* Does this model perform better or worse on out-of-sample data compared to in-sample data?

## Questions to be answered

1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?


## Conclusion -- Time Series Analysis

Based on the time series analysis, I would not feel confident buying Yen because both the ARIMA model and the ARMA model have a P > 0.05. However, the GARCH model is useful for predicting volatility.This is important when trading derivitives because as per this model it states the volatility will keep increasing in the next 5 days, therefore trading derivitives would be your best option.The GARCH model is also useful to quantify you're maximum loss as you can calculate what you're risk is in purchasing Yen.

I would not feel comfortable using these models to trade. ARMA and ARIMA are not accurate and the other is only slightly useful in a specific kind of investing.


## Conclusion -- Regression Analysis

In this particular model, The out of sample performed slightly better than the In-sample data. The Out-of-sample had a root mean squared error of 0.415, while the in-sample data has an RMSE of .596. From this data I would say the model has a "good" fit. 
