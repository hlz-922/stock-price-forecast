# stock-price-forecast

### Project Description

Forecast stock prices (2009-2019 historical data) using `Prophet` model

### Key steps

1. **Generate Forecast for Test Period**: The model is fit to the data, and a forecast is generated for the specified number of new observations. The example provided aims to forecast 252 new periods, corresponding to the number of trading days in a year. This is achieved by using the **`.make_future_dataframe`** method of the Prophet class.
2. **Produce Forecast and Plot**: With the future dates prepared, the notebook uses the **`.predict`** method to generate forecasts. These forecasts are then plotted using the **`.plot`** method to visualize the model's predictions.
3. **Compare Forecast to Historical Values**: The accuracy of the forecast is evaluated by comparing it to the actual historical values of the stock. This comparison is visualized by plotting the actual prices against the forecasted values.
4. **Cross Validation using Past Data**: To assess how well the model fits past data, cross-validation is performed. This process involves generating out-of-sample forecasts at different points in time with various forecasting horizons to understand the model's fit better. The **`cross_validation`** function from the Prophet's diagnostics module is used for this purpose, alongside the **`performance_metrics`** function to evaluate the model's performance.
