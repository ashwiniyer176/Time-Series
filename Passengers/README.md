# Airline Passenger Growth Prediction 

This is a Time Series problem where, given a year and a month, the task is to predict the number of international airline passengers in units of 1,000. The data ranges from January 1949 to December 1960, or 12 years, with 144 observations. The low dimensionality and the ease of problem domain makes this an ideal dataset to get our hands dirty with Time Series Forecasting. 
## Dataset Used

The dataset used is the [International Airline Passengers Dataset](https://www.kaggle.com/andreazzini/international-airline-passengers), which is the equivalent of Iris dataset for Machine Learning or MNIST for Computer Vision. It is a low dimensional (only 2 columns) dataset:

`Month` - Month for the observation (taken in the format `YYYY-MM`)
`Passengers` - Number of international airline passengers travelling at the time.

## Network Architecture

The Neural Network used for this problem were **Long Short Term Memory** Networks. These are capable of remembering data that has been input, unlike conventional Neural Networks, which only use input data to predict, thus LSTMs use both input data and previous historical data to make a prediction. This problem has been solved using two methods:

**1. Single Step Look Back:** The `Airline_Passengers.ipynb` shows how to get started with solving this problem by simply looking at the data point just before the current one. This is an elementary approach that works quite well for this problem.

**2. Window Look Back:** The `Airline_Passengers_Window.ipynb` shows how to take in a series of previous data points(here 3) and use them to forecast the next point. This is a more commonly used method, however for the problem at hand it gives the similar results.

**3. Retaining Memory between Batches:** The `Airline_Passengers_Window.ipynb` also has the code for making the LSTM **stateful** which basically means the network can build state over the entire training sequence and even maintain that state if needed to make predictions.