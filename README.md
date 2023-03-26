# Kriti-Stock-Price-Prediction

Built a ML model to predict Stock prices using technical indicators like EMA and RSI. The model was trained on 10 years of stock price data.

## OBSERVATIONS
- The variation in the values of the opening, closing, high andlow values of stock prices was low.
- A significant resemblance between the adjusted close and the close prices was observed. The mean difference was almost zero for companies 2 to 4. And standard deviation of difference was less than 1.
- The stock prices at the end a quarter varied significantly as compared to their values during the quarter. Hence, a new feature was created to flag the last month of a quarter.
  
  
## Feature Selection
- The Low - High data give the data about how volatile the stock price is on that day, more is the absolute difference more will be the difference in open and close.
- The quarter end plays an important role in stock price and stock price fluctuates most here so create new columns for checking wheather is it a end of qrarter.
- Volume is important as the day volume of is more , more is the activity in stock price recorded.
- Adjusted close gives an idea that the close price is around it
- Technical Indicators capture additional financial information.
  
## Why Standard Models like LSTM Fail
- Standard Models Fail because the stock prices in the starting dates were low and shot up in 2018.
- Another major problem while working on this dataset was the inclusion of prices from COVID-19 timeline, which was an unprecedented market situation causing irregular stock prices.
- It was observed that Tree-based ML algorithms and Recurrent Neural Networks failed to converge to optimal results even after training for longer duration of time due to unseen data of the future.
  
## Model Used for Final Prediction
- Hence, we switched to simpler regression models to model the data.
- Ridge Regression was chosen as it adds a regularizing parameter to avoid overfitting the data
- As the data is highly correlated, regression models seem to work well.
