# Stock Prediction 

This project follows the example given in [this article](https://towardsdatascience.com/the-complete-guide-to-time-series-analysis-and-forecasting-70d476bfe775). The Github project of the author, where the dataset is available, can be found [here](https://github.com/marcopeix/stock-prediction).

### Closing Price 

As we plot the closing price over the time period of the dataset, we can see that it is not a **stationary** process, but it is difficult to tell whether there is any **seasonality**. To capture the trend in the data, we plot the moving average. 

### Moving Average 

**Window size = 3 days**

When the window size is too small, the moving average is very similar to the actual values, making it difficult to spot any trend not already obvious on the actual values. 

![moving average 3](images/moving_average_3.png)

**Window size = 30 days**

Here, we can see a downward curve at the end, indicating that the stock is likely to go down in the following days. 

![moving average 30](images/moving_average_30.png)

**Window size = 90 days**

We can see the same downward curve here. 

![moving average 90](images/moving_average_90.png)

### Exponential Smoothing 

Here, an alpha value of 0.05 smoothed the curve while picking up most of the upward and downward trend.

![exponential smoothing](images/exponential_smoothing.png)

### Modelling 

To model the series, we must first transform it into a stationary process. First, we apply the Dickey-Fuller test to see if it is a stationary process. 

By the Dicky-Fuller test, the time series is not stationary, as we expected. From the Auto-Correlation plot, we see that auto-correlation is high and there seems to be no seasonality in the data. 

![time series analysis plot](images/time_series_analysis_plot)

Therefore, to make the process stationary and to get rid of autocorrelation, we take the first difference (subtract the time series from itself with a lag of one day). 

![time series analysis stationary plot](images/time_series_analysis_stationary_plot)

Now, our data is stationary, and we can start modelling. 


