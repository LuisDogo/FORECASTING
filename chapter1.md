# Getting Started

## What Can Be Forecasted?
Factors that make a quantity or event predictable:
- How well the factors contributing to it are understood
- Available data
- How similar the future is to the past
- Whether the forecasts affect the thing being predicted

---

| Forecast | Goal | Planning |
| --- | --- | --- |
| The prediction | What we want to happen | How to respond according to the forecast to meet the goal |

## A Good Forecast
- Captures genuine patterns and relationships within the historical data.
- Reflects the way things are changing, assuming not that the environment does not change, but that the way it is changing will continue in the future.

## Forecasting Methods
- **Qualitative forecasting**: Used when no historical data is available or relevant.
- **Quantitative forecasting**: Used when numerical information is available and it is reasonable to assume some past patterns will persist.
  - **Time series data**: Collected over time.
  - **Cross-sectional data**: Collected at a single point in time.

## Model Types
The *error* term allows us to account for random variation or unaccounted-for variables.

### Explanatory Model
$$y = f(x_1, x_2, \dots, x_n, \text{error})$$<br>
Explains the variation in the variable $y$ through the incorporation of other predictor variables.

### Time Series Model
$$y_{t+1} = f(y_t, y_{t-1}, y_{t-2}, \dots, y_{t-n}, \text{error})$$<br>
The prediction of the future is based on past values of a variable. Particularly useful when the system isn't understood or the external predictor variables have complex relationships governing the variable of interest. This model is ideal when we only care about the prediction, not why it happens.

### Mixed Model
$$y_{t+1} = f(y_t, x_1, x_2, \dots, x_n, \text{error})$$<br>
Combines the features of the above two models.

## Forecast Phases
1. **Problem Definition**
   - How will the forecast be used?
   - Who requires the forecast?
2. **Information Gathering**
   - Statistical data
   - Expertise of data collectors and forecast users
   - Note: Data value diminishes over time
3. **Preliminary (Exploratory) Analysis**
   - Start by graphing the data and searching for consistent patterns, significant trends, seasonality importance, cycles, outliers, and correlation between variables (consult experts to explain these).
4. **Choosing and Fitting Models**
   - Compare 2–3 potential models. Each model is an artificial construct based on a set of assumptions (explicit and implicit), involving parameters to be estimated using known historical data.
5. **Using and Evaluating a Forecast Model**
   - Once the model and its parameters are chosen, the model's performance can only be evaluated after the data for the forecast period becomes available.

## Forecasting Point of View
What we are trying to forecast is unknown and can be thought of as a *random variable*. When we obtain a forecast, we are estimating the middle of the range of possible values that the random variable can take. This forecast is accompanied by a *prediction interval* that gives a range of possible values the random variable can take with high probability.

$$y_t$$: Observation at time *t*.<br>
$$I$$: All information we have observed.<br>
$$y_t|I$$: The random variable $$y_t$$ given what we know in $$I$$.<br>

The set of values that the random variable $y_t$ can take, along with their respective probabilities, is known as the *probability distribution* of $$y_t|I$$ and is referred to as the *forecast distribution*.<br>

$$\hat{y}$$: Forecast, the average value of the forecast distribution.<br>
$$\hat{y}_{t|t-1}$$: Forecast of $$y_t$$ given all previous observations $$(y_1, \dots, y_{t-1})$$<br>
$$\hat{y}_{T + h|T}$$: Forecast of $$y_{T + h}$$ taking into account $$y_1, \dots, y_T$$.<br>
