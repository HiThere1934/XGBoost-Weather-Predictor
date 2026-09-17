# XGBoost-Weather-Predictor
Simple Temperature Predictor using XGBoost and Open Meteo API data

The program obtains weather data using Open Meteo's free API. It then creates a dataframe using this data, processing specific features that interact non-linearly with Daily Minimum Temperatures (eg Wind Direction, used Sine function to make sure model understands the gap between 0 and 359 degrees is not as massive as it would seem if looked at linearly). 

The program splits the data set into a training and testing set, then normalizes every input feature for the training data set except for dates before feeding into the XGBoost model to prevent testing data from contaminating the training data. 

Matplotlib is then used to plot the Expected vs. True minimum temperature, and an R^2 and RMSE value is derived. 
