# TIME SERIES DECOMPOSITION
time series are complex, so we dissect them into components representing and underlying pattern category.
- data = $y_t$
- seasonal component = $S_t$
- trend = trend + cycle = $T_t$
- remainder component = white noise $R_t$

Additive composition:  $$y_t = S_t + T_t + R_t$$
Magnitude of seasonal fluctiations & variation around trend cycle dont vary with the time series level.
<br>

Multiplicative composition:  $$y_t = S_t * T_t * R_t \equiv log(y_t) = log(S_t) + log(T_t) + log(R_t)$$
Magnitude of seasonal fluctiations & variation around trend cycle vary with the time series level.
<br>
## Methodology
1. transform/adjust it
2. decomposition it
3. analyze it
## Transformations/adjustments
we do this, to obtain a simpler series by removing known sources of variation/making the pattern more consistnet across the data. There are 4 kinds of transformations:
- calendar (average per day)
- population (per - capita)
- inflation (price index "dollar values from a particular year")
- mathematical (log, power, box-cox) if the data shows variation which increases or decreases with the level of the series

<br>*simpler patterns are easier to model & yield better forecasts*

## Decompositions
- unavailable estimations for first/last few observations.
- oversmooths big changes in trend-cycle
- unable to capture seasonal changes over time.
- not robust enough to capture atypical values.
### Moving Averages
- OG time series decomposition method
- estimates tred-cycle (capturing main movement, without minor fluctuations)
### Smoothing m-**MA**
estimate of trend-cycle component at time t, m observation window centered on the t observation.
$$\^T_t = \frac{1}{m} \sum_{j = -k}^k y_{t + j}$$
where m = 2k + 1
- odd number.
- close in time $\approx$ close in value
- averaging eliminates randomness in data, leaving the smooth trend-cycle component.
- m $\alpha$ smoothness
### Moving Average of Moving Average
- mxn-**MA** = m-**MA** applyed after an n-**MA**
- even number
### Weighted Moving Averages
- result as combinations of nm-**MA**
### Classical Decomposition
We assume that the seasonal component is constant from year to year
#### Additive
#### Multiplicative
### Modern Decomposition Methods
- X-11
    - **Additive & Multiplicative support**
    - available estimations for all times
    - seasonal component is allowed to vary over time (slowly)
- SEATS
    - "Seasonal Extraction in ARIMA time series"
- STL
    - **Additive support**
    - handles all seasonality types.
    - seasonal component rate of change & smoothness of trend-cycle are hyperparameters
    - robust against outliers