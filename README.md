# mod_4_Time_Series
Overview:
   This project was designed to explore time series models: SARIMAX,Prophet. Our idea was to analyze a small cap security that has an agriculture product. The goal was to use exogenous variables to improve our model. The stock we selected was Farmer Brothersf company ticker: FARM. They are a wholesaler of coffee and tea.  The variables we used to help us predict were as follows: coffee bean index, tea index, monthly rainfall in Nicaragua, ten year bond prices. After researching where the coffee came from and the biggest factor in strong coffee yields, we found that rainfall in Nicaragua was a factor worth including. We wanted to include interest ratings and went with a ten year bond etf to help simulate an interest rate effect. Prices of coffee and tea were included with index's of each that we found.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.55.39%20PM.png) 
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-06-03%20at%2010.15.29%20AM.png)
   
Stationary our data:
    We checked our data with a Dicky Fuller test to see if our data was non stationary. After we took a differencing of 1 we were able to improve the Stationarity of the data for our models.  
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%206.53.46%20PM.png)
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.56.02%20PM.png)
 !![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-06-03%20at%2010.15.18%20AM.png)
 The Dicky Fuller test before the differencing and after show an improvement in the numbers. The graph visually demonstrates the effect.
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.55.54%20PM.png)
SARIMAX:
  We first ran a SARIMAX model to see how well our exogenous variables would perform. We put together a pipeline of different combinations to check the AIC score for our best model. After running the SARIMAX model we found that the TEA index was the only one with a p-value that we could use.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%207.22.03%20PM.png)
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%2012.17.40%20PM.png)
  Our mean squared error was improved overall:
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%209.56.45%20AM.png)
Prophet:
  Our final model was the facebook Prophet model. It took all of our exogenous and made what looked like a rolling mean prediction. They stock took a dive right where we started predicted which made it a much tougher prediction.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%206.08.38%20PM.png)
  
 Silver lining & Next steps:
  After reviewing monthly price data vs monthly prediction data we found that 7 out of 11 time periods we correctly predicted the direction of the stock. For our next steps we are going to group our exogenous variables in different time buckets and look for news articles that come out that the market might not be factoring into the price.
    
    
    
    
 
