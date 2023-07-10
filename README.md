# Kriti-Stock-Price-Prediction

Built an ML model to predict Stock prices using technical indicators like EMA and RSI. The model was trained on 10 years of stock price data. The initial phase included extensive Exploratory Data Analysis.

### Plotting the entire datasets of all four companies
![plot1](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/3bcfc4f9-0c49-4390-b2f2-edaf167d6949)
![plot2](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/40cc0931-ef39-4075-bfaa-d53cbf08b8e3)
![plot3](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/2870d2c6-baa6-41aa-9d90-f0363ac3ca78)
![plot4](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/13c80943-9e7a-4a5e-94e9-6f37b23e8c6f)

### Taking a closer look at recent data
![plot5](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/a2272a7d-d8df-4be5-97b6-02bfd784486d)
![plot6](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/1cb51b42-41ba-4cfe-882f-21c5b002bd22)
![plot7](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/9660199c-b594-470b-ba28-1629e6f62771)
![plot8](https://github.com/achintya7567/Kriti-Stock-Price-Prediction/assets/42384065/38f4f885-df11-4342-b71e-191d63afdf68)


## OBSERVATIONS
- The variation in the values of the opening, closing, high and low values of stock prices was low.
- A significant resemblance between the adjusted close and the close prices was observed. The mean difference was almost zero for companies 2 to 4. And the standard deviation of difference was less than 1.
- The stock prices at the end of the quarter varied significantly as compared to their values during the quarter. Hence, a new feature was created to flag the last month of a quarter.
  
  
## Feature Selection
- The Low - High data give the data about how volatile the stock price is on that day, the more the absolute difference more will be the difference in open and close.
- The quarter end plays an important role in stock price and the stock price fluctuates most here so create new columns for checking whether is it the end of quarter.
- Volume is important as the day volume is more, more is the activity in stock price recorded.
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
