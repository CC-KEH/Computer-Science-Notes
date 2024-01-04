## Introduction

Moving average is a statistical technique commonly used in time series analysis to smooth out short-term fluctuations and highlight longer-term trends or cycles. It involves calculating the average of a subset of data points within a moving window or interval, and as the window moves through the data, a series of averages is obtained.

![[Pasted image 20240104165620.png]]

## Types of Moving Averages

### 1. **Simple Moving Average (SMA):**
   - The SMA is calculated by taking the arithmetic mean of a fixed set of data points over a specified period.

   ![[Pasted image 20240104004852.png]]

   - Xt represents the data point at time t, and n is the number of periods.

### 2. **Weighted Moving Average (WMA):**
   - The WMA assigns different weights to different data points within the moving window. It emphasizes certain data points more than others.
![[Pasted image 20240104004935.png]]

   - wi represents the weight assigned to the data point Xt-i.

### 3. **Exponential Moving Average (EMA):**
   - The EMA gives more weight to recent data points and exponentially decreases the weights as you go back in time.

  ![[Pasted image 20240104005050.png]]

   - alpha is the smoothing factor, and a higher value gives more weight to recent observations.

### 4. **Centered Moving Average (CMA):**
  - Unlike the simple moving average, which places equal weight on all data points within a window, the centered moving average gives more weight to the central data point in the window, providing a more accurate representation of the underlying trend.
![[Pasted image 20240104164501.png]]
 - The CMA for a data point Xt​ with a window size of n is calculated as the average of the values within a symmetric window centered around Xt​:

## Applications

1. **Smoothing Time Series Data:**
   - Moving averages are used to eliminate noise and highlight trends in time series data, which later helps in pattern recognition for better analysis.

2. **Forecasting:**
   - Predicting future values by analyzing the trend captured through moving averages.

3. **Technical Analysis in Finance:**
   - Analyzing stock prices and financial data to identify trends and potential buy/sell signals.

4. **Economic Indicators:**
   - Analyzing economic indicators over time to identify patterns and trends.

5. **Demand Planning:**
   - Forecasting demand for products based on historical sales data.

## Considerations

1. **Choice of Window Size:**
   - The size of the moving window impacts the level of smoothing and responsiveness to changes. Larger windows provide smoother trends but may lag behind changes.

2. **Weight Selection (for WMA):**
   - When using weighted moving averages, the choice of weights affects the importance given to different data points.

3. **Exponential Smoothing Factor (for EMA):**
   - The smoothing factor in EMA determines the weight given to the most recent observation. The choice of this factor influences the responsiveness of the average to changes.

4. **Data Stationarity:**
   - Moving averages are most effective when the underlying time series data is stationary (constant mean and variance).