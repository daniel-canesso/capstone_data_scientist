# Capstone Project - Predict Bitcoin Value

### Requirements
- pandas
- sqlalchemy
- itertools
- numpy
- sklearn
- seaborn
- matplotlib

### Files

- Prepare and Import Data : prepare, clean and import data
- Exploratory: exploratory analysis 
- Model: model created


### Motivation

Predicting the closing price of various assets is one of the first things every data scientist tries to do at least once in his career. The world of trading is fascinating, and poses immense challenges for us. The area of trading by algorithms has been gaining strength for some years, and this is the motivation of this work. Create a model that is able to predict, with reasonable accuracy, the closing price of the Bitcoin asset, in daily time, and using only the price data.

The model evaluation metric chosen by the percentage error of the entire historical series, and which must be below 5%.

### Conclusion

In the present work, the construction of a model that aimed to predict the next day's closing price, using data from the day or previous days, was conceived. The model error, and evaluation metric, is the percentage error between the actual value and the predicted value. We idealized that the error should be below 5% when we look at the average of the entire historical period.

The model is based on linear regression, and uses data from X previous periods (days) for training, using only the last day to forecast the next day's closing. In this way, we will always have a training and test set.

A function was built so that the best model could be found, testing a variation between periods and between columns that could be used as predictor variables. Based on these tests, we found the best model, which was using 29 periods and only the "close" column.

The model was then retrained, and a new dataframe was built with forecast, absolute error and percentage error columns.

Based on this new dataframe, and error measures, we verified that the average error obtained was below our target, which was 5%, as well as the median.

The error measures found were:

- Average of errors: 2.77%

- Median of errors: 1.7%

The biggest deviations between the model's prediction and reality occurred on days when the market suffered some distortions, caused mainly by what in the world of trades are called "whale movements", and the price came to vary by more than 30% of overnight.

We concluded that the performance of the model was satisfactory, and we considered our study to be valid, since we stayed within the desired error metric.


### Link for article

https://daniel-bicalho.medium.com/bitcoin-value-prediction-a8753764dabd

