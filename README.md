# Stock Prediction 

This project follows the example given in [this article](https://towardsdatascience.com/the-complete-guide-to-time-series-analysis-and-forecasting-70d476bfe775). The Github project of the author, where the dataset is available, can be found [here](https://github.com/marcopeix/stock-prediction).

### Closing Price 

As we plot the closing price over the time period of the dataset, we can see that it is not a **stationary** process, but it is difficult to tell whether there is any **seasonality**. To capture the trend in the data, we plot the moving average. 

### Moving Average 

**Window size = 3 days**

![moving average 3](images/moving_average_3.png)

**Window size = 30 days**

![moving average 30](images/moving_average_30.png)

**Window size = 90 days**

![moving average 90](images/moving_average_90.png)