## Auto-Correlation Function (ACF)

### Introduction

The Auto-Correlation Function (ACF) is a statistical tool used in time series analysis to measure the correlation between a time series and its lagged values. It provides insights into the temporal dependencies and patterns within the data.

### Key Concepts

1. **Correlation at Different Lags:**
   - ACF calculates the correlation coefficients between a time series and its lagged values at various time intervals.

2. **Lag:**
   - The time difference between the original observation and the observation being compared.

3. **ACF Plot:**
   - A graphical representation of auto-correlation coefficients against corresponding lags.

### Calculation

- For each lag \(k\), the auto-correlation coefficient (rho_k) is calculated using the formula:

   ![[Pasted image 20240104183216.png]]
   - Yt is the value at time t, Cov is the covariance, and Var is the variance.

### Interpretation

- **Positive ACF:** Indicates a positive correlation between the current value and the lagged value.

- **Negative ACF:** Indicates a negative correlation between the current value and the lagged value.

- **Zero ACF:** Indicates no linear relationship between the current and lagged values.

### ACF Plot Patterns

1. **Randomness:**
   - In a random series, auto-correlation coefficients at all lags are close to zero.

2. **Seasonality:**
   - Periodic spikes at regular intervals suggest seasonality.

3. **Trend:**
   - A gradual decrease or increase in auto-correlation suggests a trend.

## Partial Auto-Correlation Function (PACF)

### Introduction

The Partial Auto-Correlation Function (PACF) is a tool used in time series analysis to measure the correlation between a time series and its lagged values, controlling for the effects of other lags. It helps identify the direct relationship between a variable and its lag.

### Key Concepts

1. **Partial Correlation:**
   - PACF calculates the correlation between a variable and its lag, controlling for the effects of other lags.

2. **Lag:**
   - The time difference between the original observation and the observation being compared.

3. **PACF Plot:**
   - A graphical representation of partial auto-correlation coefficients against corresponding lags.

### Calculation

- The PACF is often computed using recursive linear regression. For example, the PACF at lag \(k\) is the correlation between \(Y_t\) and \(Y_{t-k}\) after removing the effects of lags \(1, 2, \ldots, k-1\).

### Interpretation

- **Partial Auto-Correlation at Lag 0:** Equals the correlation coefficient between \(Y_t\) and itself, which is 1.

- **Partial Auto-Correlation at Lag \(k\):**
   - Measures the correlation between \(Y_t\) and \(Y_{t-k}\) after removing the effects of lags \(1, 2, \ldots, k-1\).

### PACF Plot Patterns

1. **Identification of AR Processes:**
   - PACF is particularly useful in identifying autoregressive (AR) processes.

2. **Sharp Cutoffs:**
   - Sudden drops in partial auto-correlation indicate the direct effect of the specified lag.

## Applications

1. **Model Identification:**
   - ACF and PACF are crucial for identifying potential models for time series analysis, such as autoregressive (AR) or moving average (MA) models.

2. **Seasonal Analysis:**
   - Identifying seasonality patterns in time series data.

3. **Forecasting:**
   - ACF and PACF are used to understand the relationship between current and past values for predictive modeling.

## Considerations

- **Interpretation Together:**
   - ACF and PACF are often used together for a more complete analysis of time series data.

- **Stationarity:**
   - ACF and PACF can provide insights into the stationarity of the time series.

- **Outliers:**
   - Outliers in the data can influence ACF and PACF results.