# Fundamental Statistical and Machine Learning Models for Time Series Analysis
## November 1, 2022
## Jeffrey Yau, PhD
---
### Notes

- Divide time series data into two parts
    - Historical observatinal periods - past data of the series of interest and exongenous series data
    - Forecast period - future
- Time series forecasting requires models
    - Forecast horizon <i>H</i> - how far away are we going to forecast
    - Forecast origin <i>t</i> - when are we starting our predictions
    - Current information set () - series of interest + exogenous data
- Persistent forecast - using the last observation (forecast origin - 1 observation) as the prediction (better be able to beat this)
- Rolling average model - average of values from pre-defined, past <i>k</i> time periods
- <b>Autoregressive Integreated Moving Average (ARIMA)</b>
    - Useful for modeling one series
    - Series can be made “stationary” by differencing
    - Perhaps in conjunction with nonlinear transformations such as logging or deflating
    - A time series is stationary if its statistical properties are all constant over time 
    - A stationary series has no trend, its variations around its mean have a constant amplitude, and it wiggles in a consistent fashion, i.e., its short-term random time patterns always look the same in a statistical sense.
    - General steps
        - Ingest the series
        - Train/validate/test split the series
        - Conduct exploratory time series data analysis on the training set
        - Determine if the series are stationary
        - Transform in ont stationary
        - Build model
        - Model diagnostic
        - Model selection
        - Make forecast
        - Inverse-transformt the forecast
        - Forecast evaluation
- <b>Vector Autoregressive (VAR) Model</b>
    - Useful for multivariate time series analysis
    - Model dynamic properties and interseries relationships
    - Only applies to stationary series (transform series if not stationary)
    - Note - Difference transformation generates missing values
- <b>Recurrent Neural Network (RNN)</b>
    - Traditional neural networks lack a mechanism to account for time of observations
    - RNNs retain past information, track and update the state of the world
    - Christopher Olah's blog on LSTMs https://colah.github.io/posts/2015-08-Understanding-LSTMs/
    - 

### Investigate
- Macroeconomics and Reality - Christopher A. Sims

