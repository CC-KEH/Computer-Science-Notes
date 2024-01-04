## Stationary Time Series

### Definition

- **Stationarity:** A time series is considered stationary if its statistical properties, such as mean, variance, and autocorrelation, remain constant over time.

### Characteristics

1. **Constant Mean:**
   - The average of the time series data points remains constant over time.

2. **Constant Variance:**
   - The variability or dispersion of the data points around the mean remains constant.

3. **Constant Autocorrelation:**
   - The correlation between the observations at different time points remains constant.

### Importance

- **Easier Modeling:** Stationary time series are easier to model and analyze using statistical methods, and many time series models assume stationarity.

- **Predictability:** Stationary series are more predictable, as their statistical properties do not change over time.

## Non-Stationary Time Series

### Definition

- **Non-Stationarity:** A time series is considered non-stationary if its statistical properties change over time, indicating trends, seasonality, or other systematic patterns.

### Characteristics

1. **Trend:**
   - A consistent upward or downward movement in the data over time.

2. **Seasonality:**
   - Repeating patterns or cycles that occur at regular intervals.

3. **Time-Varying Variance:**
   - The variability of the data points changes over time.

### Challenges

- **Modeling Complexity:** Non-stationary series require more sophisticated models, as the statistical properties change over time.

- **Unpredictability:** Non-stationary series can be less predictable, making forecasting challenging.

## Tests for Stationarity

### 1. **Visual Inspection:**
   - Plotting the time series data and observing trends or seasonality.

### 2. **Summary Statistics:**
   - Comparing mean and variance across different time periods.

### 3. **[[Augmented Dickey-Fuller Test]]:**
   - A statistical test that checks for the presence of a unit root in a time series, indicating non-stationarity.

### 4. **Kwiatkowski-Phillips-Schmidt-Shin (KPSS) Test:**
   - A test that checks for stationarity around a deterministic trend.

## Strategies for Stationarizing Time Series

1. **Differencing:**
   - Taking the difference between consecutive observations to remove trends.

2. **Seasonal Adjustment:**
   - Removing seasonal components to achieve stationarity.

3. **Transformation:**
   - Applying mathematical transformations (e.g., logarithmic) to stabilize variance.

4. **Detrending:**
   - Removing the trend component from the time series data.
