# Forecasting-SPY
Using a Long Short-Term Memory (LSTM) Recurrent Neural Network (RNN) to forecast the price of the S&amp;P 500 index

## Data
No external data download is needed, courtesy of the [yfinance](https://pypi.org/project/yfinance/) library.   
The baseline model only uses OHLCV data.

## Installing Libraries
Make sure you satisfy the system requirements and are using the correct python version before downloading. 
```python
pip install -r requirements.txt
```

## Baseline Prediction
#### Baseline Function
- Prediction: One Step (next trading day)
- Activation Function: Linear 
- Lookback Period: One year
- Steps: 70

![one-step](https://raw.githubusercontent.com/DestrosCMC/Forecasting-SPY/main/assets/base/oneStep.png)
#### Output:
```
Mean Absolute Error: 226.74624230089194
Future price after 1 days is 362.72$
1: Accuracy Score: 0.5555555555555556
```
### Interpretation:
The accuracy score of the one step prediction model is 55.6%. This is a 5.6% improvement over the 50% chance the price of the SPY goes up or down.\
This is a substantial improvement, but as I will show in later excercises the longer the forecast window (e.g. 1 month) the more accurate a prediction.

### Inspiration:
[Price Prediction Tutorial](https://www.thepythoncode.com/article/stock-price-prediction-in-python-using-tensorflow-2-and-keras)\
Thank you to PythonCode for many of the functions used in this educational model. 
