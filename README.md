# Weather Prediction and Model Comparison

The project aims to understand weather patterns in the city of Tours during 2000-2009. Different machine learning models are used to predict temperature, and compare their performance. 

## Approach

** Exploratory Data Analysis

1. Observing the mean, maximum, minimum and diurnal temperatures. From the charts we can observe some significant peaks and dips that deviate from the normal trends.
   ![Mean temperature 2000-2009 in Tours](charts/Mean temperature 2000-2009 in Tours)
   ![Mean,Maximum,Minimum and Diurnal temperatures in Tours 2000-2009](charts/Mean,Maximum,Minimum and Diurnal temperatures in Tours 2000-2009.png)

2. Observing the average precipitation and humidity recorded from 2000-2009. Some years have below average precipitation, while some years proved to be more humid than others.
   ![Average precipitation 2000-2009](charts/Average precipitation 2000-2009.png)
   ![Average humidity 2000-2009](charts/Average humidity 2000-2009.png)

3. From the charts above, we observed some spikes in temperature in 2003 and some drops in 2009. So we individually analyse those years.
   ![Comparison of Temperature, Precipitation and Humidity in 2003](charts/Comparison of Temperature, Precipitation and Humidity in 2003.png)
   ![Comparison of Temperature, Precipitation and Humidity in 2009](charts/Comparison of Temperature, Precipitation and Humidity in 2009.png)

4. Observing the outliers.
   ![Temperature Anomalies per Month](charts/Temperature Anomalies per Month.png)

5. Using autocorrelation to observe the temperature of day n on n-1, and performing seasonal decomposition.
   ![ACF PACF raw mean temperature](charts/ACF PACF raw mean temperature.png)
   ![Seasonal Decomposition](charts/Seasonal Decomposition.png)

** Modelling and Evaluation

To predict temperature, Ridge, GradientBoostingRegressor and Random Forest were used. The years 2000-2006 were set as training period and the years from 2007-2009 were used as test dataset. A baseline was established for further evaluation. MAE and RMSE were used as evaluation metrics, and it was observed that all 3 models performed better than the baseline, however GradientBoostingRegressor, turned out to be the best performing.

![Model Evaluation](charts/Model performance.png)

For better comprehension, user input was taken and the original temperature was compared with the returned prediction of each model.



   

   
   

![Model comparison](images/model_comparison.png)
