
# Unit 10: A Yen for the Future

In this assignment, we tested some time series tools in order to predict future movements in the value of the Canadian dollar versus the Japanese yen

## TIME SERIES ANALYSIS

#### Return Forecasting: Time Series Analysis & Modelling with CAD-PHY Exchange rate data.
In this notebook, you will load historical Canadian Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

![CAD JPY PLOT](images/cad_jpy_plot.png)

**Question: Do you see any patterns, long-term and/or short?**

**Answer:** Since the 1996 bottom of CADJPY, there appears to be major whipsaw action before a crash beack down. This is likely longterm consolidation before a major move as typically (from a technical analysis perspective), price action tests the trend line 5x before a break out or breakdown. Additionally, we have been rangebound between 70-110 for almost 25 years.

![PVS PLOT](images/pvs.png)
**Question: Do you see any patterns, long-term and/or short?**

**Answer:** The trend looks very similar to an EWMA. There was a large trend break at the end of 2016, but the price action seems heavy, without strength. It could not reverse.

![ReturnForecase](images/CADJPY_Return_Forecast.png)

**Question: Based on the p-value, is the model a good fit?**

**Answer:** In our ARMA model above, the autoregressive term has a p-value 0.807, which is much more than 0.05. Therefore, it is not statistically significant, and is not a reliant model. To be considered a good model, P < 0.5.

![CADJPY_5Day_Forecast](images/CADJPY_5Day_Forecast.png)

**Question::** What does the model forecast will happen to the Japanese Yen in the near term?

**Answer:** The line graph demonstrates that the CADJPY will fall over the next 5 sessions. However, P = 0.458 which is not statistically significant.

## Conclusions

**1 - Based on your time series analysis, would you buy the yen now?**

Based on both the ARMA and ARIMA models, the CADJPY will trend down in the coming sessions. Additionally, the GARCH model indicates that volatility will increase. Therefore, I wouldnt' buy the yen.

**2 - Is the risk of the yen expected to increase or decrease?**
Risk in the yen is expected to increase due to the rising volatility.

**3 - Based on the model evaluation, would you feel confident in using these models for trading?**

Although I appreciate the exercise of utilizing these models, both coefficients and statistical significance of these models indicate they are unreliant.

## REGRESSION ANALYSIS

### Conclusions

**Question: Does this model perform better or worse on out-of-sample data as compared to in-sample data?**

**Answer:** The out-of-sample RMSE (.6445) is lower than the in-sample RMSE (0.84). RMSE is typically lower for training data, but is higher in this case. This means the model made better predictions on data it has never seen before (the test set) than the actual training set. I would not trust these models.