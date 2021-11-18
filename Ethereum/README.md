
# Predicting Ethereum Prices

Ethereum is a decentralized, open-source blockchain with smart contract functionality. Ether (ETH or Ξ) is the native cryptocurrency of the platform. After Bitcoin, it is the largest cryptocurrency by market capitalization. Ethereum is the most actively used blockchain. Ethereum was proposed in 2013 by programmer Vitalik Buterin.


## Dataset

The dataset used is the [Ethereum USD Dataset](https://www.kaggle.com/varpit94/ethereum-data) from Kaggle. The trading data shown is at the day level.

**Columns**

1. **Date:** Date 
2. **Open:** Price from the first transaction of a trading day
3. **High:** Maximum price in a trading day
4. **Low:** Minimum price in a trading day
5. **Close:** Price from the last transaction of a trading day
6. **Adj Close:** Closing price adjusted to reflect the value after accounting for any corporate actions
7. **Volume:** Number of units traded in a day

## Network Architecture

The Neural Network used for this problem were **Long Short Term Memory** Networks. These are capable of remembering data that has been input, unlike conventional Neural Networks, which only use input data to predict, thus LSTMs use both input data and previous historical data to make a prediction. This problem has been solved using two methods:

**Window Look Back:** The `Ethereum_prices.ipynb` shows how to take in a series of previous data points(here 3) and use them to forecast the next point. This is a more commonly used method, however for the problem at hand it gives the similar results. We use the closing prices of ETH for the past 3 days to predict the ETH price of the next day,
