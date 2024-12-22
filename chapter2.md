# TIME SERIES GRAPHICS
In data analysis we plot first, ask second. <br>
Features seen in plots must be incorporated as much as possible  in the forecasting methods used.
## Variable types
| index | key | value |
|---|---|---|
| recording time | composite id | measured quantity |

for each unique combination of key variables we can create a time series. 
## Time series patterns
- *trend*: long-term direction.
- *season*: unchanging frequency associated with some aspect of the calendar.
- *cycle*:pattern is not a fixed fluctuation.
## Graphs
### Time plots
observations plotted against the time of observation
### Seasonal plots
data is plotted against each individual "season" observed.
the data can have more than one seasonal pattern(season can contain seasons), we can plot according to the granularity required.
### Scatterplots
explore relationships between time series by plotting them against each other, it's common to compute some correlation coefficient along the scatterplot, the correlation and the scatterplot complement eachother.
### Lag plots
display the values of the time series at $$y_t$$, plotted against  $$y_{t - k}$$ where k is the lag, these are closely related to *autocorrelation* which measures relationships between lagged values of a time series. $$r_k$$: autocorrelation coefficient for lag $$k$$, the autocorrelation coefficients make up the *AutoCorrelationFunction*.
### ACF plots
portrays the:
- Trend: positive values that slowly decrease over time as lag increases.
- Seasonality: higher autocorrelations for seasonal lags than for other lags. 
of a time series.
## White noise
time series that show no autocorrelation.
For "white noise" series we expect  $$95\%$$ of the spikes of the ACF to lie within $$\pm2\sqrt[2]{T}$$ where:$$T$$ is the length of the time series, if $$1+$$ are outside these bouds or more than $$95\%$$ of the spikes are outside these bounds , the series is probably not white noise.
