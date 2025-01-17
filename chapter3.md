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
