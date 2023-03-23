

 ***MACHINE LEARNING AND PREDICTING EXCHANGE RATES***
 
     Presented by:
 
     ** Alex Leonov, Manan Wala, Ritvik Thakur, Thi Minh Thu Nguyen, Abdullah Aldahhan

* Motivation & Summary Slide

 Exchange Rates are an integrall part of International Economics and the Stock Market. There are multiple factors that affect the excahnge rate between any 2 countries. Our goal was to evaluate the most known parametes that affect Excahnge Rates: CPI (Consumer Price Index), Foreign Reserves, and Prime Rates. Additionaly Crude Oil Prices, SP500 index, and S&P/TSX Composite data was prepared for further analysis. Our goal was to use this data to predict the future Exchange Rate Between Candian Dollar and American Dollar. Historicall Data after 1970 was used for our analysis.
      
 We divided our data into daily and monthly data. For example CPI and Foreign Reserves was compared to the average exchange rate for the month (as MONTHLY data), and Prime Rates were analysed on a daily basis.
  
  

* Model Summary

Our team used multipe models to evaluate the historical monthly and daily data and make predictions:
  
      * Cluster Analysis
      * Linear Regression with redictions
      * Random Forest
      * Gradient Boosting Regression
      * Neural Networks (NN model)
      * Super Vectore Machines
      * K-Nearest Neighbors (KNN)
      

* Data Cleanup & Model Training

Our data came mostly from Capital Iq.

Despite having some uniformity, there were challenges with preparing the data for analysis:

**Data Prep

-Dates had to be coded to be unifrom (Datetime). For example, monthly data had to be stripped of 'days' and only left with 'year' and 'month'
-Searching for and dropping: Nulls, Nan, and "-"
-Splitting data, Rearanging, Concatenating (merging), and Renaming
-Finding diffrences for data of 2 countries

**Model Training

-Figuring out evaluation metrics and incorporating into each model was also time-cosuming.
-Determining independent variables and compilation process.



* Model Evaluation

Multiple Techniques were used to evaluate the diffrent models:

MAE, MSE, RMSE, and R-squared are common evaluation metrics used in machine learning regression problems that were used in this case.

MAE (Mean Absolute Error) is the average absolute difference between the predicted values and the actual values. It measures the average magnitude of the errors in a set of predictions, without considering their direction. The lower the MAE value, the better the model's performance.

MSE (Mean Squared Error) is the average of the squared differences between the predicted values and the actual values. It measures the average squared difference between the predicted and actual values, and it penalizes larger errors more heavily than smaller ones. The lower the MSE value, the better the model's performance.
RMSE (Root Mean Squared Error) is the square root of the MSE. It measures the standard deviation of the residuals (prediction errors). The lower the RMSE value, the better the model's performance.

R-squared (Coefficient of Determination) is a statistical measure that represents the proportion of variance in the dependent variable that is explained by the independent variables in a regression model. It ranges from 0 to 1, with higher values indicating a better fit of the model to the data. A value of 1 means that the model explains all the variability of the response data around its mean. A value of 0 means that the model explains none of the variability.

In general, it is better to have lower values for MAE, MSE, and RMSE, as it indicates a smaller prediction error. For R-squared, a higher value indicates a better fit of the model to the data, but it's important to note that a high R-squared does not necessarily mean that the model is a good predictor, as it may be overfitting the data.


* Discussion

Overall, Random Forest was the best model to fit our data.

No model was good at predicting Monthly Data. The most likely reason is that only approximately 800 data points were available for training and testing.

All models had a better prediction rate with The Daily Data which had over 10,000 data points. Based on MAE, MSE, RMSE, and R-squared, overall, Random Forest was the best model to fit our data.

Further Analysis (Training and Testing) is required to determine the most ultimate model.


* Postmortem

  
Many unanswered questions remain:

-Which other variables could effect and explain the variation in teh CAD/USD Exchange rate? For example, 10-year bond yeild.
-What if we combined all daily and monthly variables and used a more sophisticated ML algorithm?
-Would our findings hold true for other currency pairs?
-Integrating our findings into automated trading or Roboadvisor platform based on live API's



