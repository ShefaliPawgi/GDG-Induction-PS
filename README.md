# GDG-Induction-PS
the PS solutions submitted by Shefali Pawgi

# GDG-Induction-PS
the PS solutions submitted by Shefali Pawgi

PS 1, TASK 1
The problem - to model the uncertainty and volatility inherent in financial assets and to develop a forecasting engine that learns from historical market data to predict future trends for a specific period

So i first download AAPL stock prices from yahoo finance and then convert it into csv and then into pandas dataframe.

I convert the closing prices from string to float and compute returns.
then i use the ADF test for stationarity. the p value is very, very less, indicating the series is stationary
then i plot the prices and log returns
the ACF and PACF plots reveal no significant autocorrelation, so arima or AR or MA wont be useful here.( i tried them and got really trivial results.)

then i started researching about arch , garch etc and found that this is quite useful as it models the uncertainty in the series.

the AIC and BIC are used to compute the order of the garch model required.
i have scaled the returns and then trained my model on training dataset and then used rolling forecast validation.
then there are some testing metrics like QLIKE, MAE, MSE etc.
in the end we have graphs for predicted volatility and confidence bands and lastly the actual prices for the predicted days.


