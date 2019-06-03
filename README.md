# mod_4_Time_Series
Overview:
   This project was designed to explore time series models: SARIMAX,Prophet. Our idea was to analyze a small cap security that has an agriculture product. The goal was to use exogenous variables to improve our model. The stock we selected was Farmer Brothersf company ticker: FARM. They are a wholesaler of coffee and tea.  The variables we used to help us predict were, coffee bean index, tea index, monthly rainfall in Nicaragua, ten year bond prices.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.55.39%20PM.png) 
   
   
Stationary our data:
    We checked our data with a Dicky Fuller test to see if our data was non stationary. After we took a differencing of 1 we were able to improve the Stationarity of the data for our models. 
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%206.53.46%20PM.png)
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.56.02%20PM.png)
 ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%205.55.54%20PM.png)
SARIMAX:
  We first ran a SARIMAX model to see how well our exogenous variables would perform. We put together a pipeline of different combinations to check the AIC score for our best model. After running the SARIMAX model we found that the TEA index was the only one with a p-value that we could use.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%207.22.03%20PM.png)
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%2012.17.40%20PM.png)
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%209.56.45%20AM.png)
Prophet:
  Our final model was the facebook Prophet model. It took all of our exogenous and made what looked like a rolling mean prediction. They stock took a dive right where we started predicted which made it a much tougher prediction.
  ![plot](https://github.com/denisdunn/mod_4_Time_Series/blob/master/Screen%20Shot%202019-05-30%20at%206.08.38%20PM.png)
  
 Silver lining:
  After reviewing monthly price data vs monthly prediction data we found that 7 out of 11 time periods we correctly predicted the direction of the stock.
    
    
    
    
 
