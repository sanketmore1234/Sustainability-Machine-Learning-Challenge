# Sustainability-Machine-Learning-Challenge
Though a little late in the day, the world is waking up to the deleterious effect of fossil fuels on our environment. As the doomsday clock ticks away, human beings are turning to renewable energy to avert a possible apocalypse. Fortunately, the sun is a well-spring of clean energy. 

Taking the cue, Wipro, in association with MachineHack, has designed a forecasting challenge to optimise solar power generation using ML models.  A solar power generation company wants to optimize solar power production and needs the prediction model to predict ‘Clearsky DHI’, ‘Clearsky DNI’, ‘Clearsky GHI’. The data is ten years at an interval of every 30 mins with the following data points:  

['Year', 'Month', 'Day', 'Hour', 'Minute', 'Temperature', 'Clearsky DHI', 'Clearsky DNI', 'Clearsky GHI', 'Cloud Type', 'Dew Point', 'Fill Flag', 'Relative Humidity', 'Solar Zenith Angle', 'Pressure', 'Precipitable Water', 'Wind Direction', 'Wind Speed']


# Objective
Predict 'Clearsky DHI', 'Clearsky DNI', 'Clearsky GHI'

# Libraries Used
1. Pandas
2. Datetime
4. Scikit Learn
5. Matplotlib
6. Numpy
7. Pickle
8. XGBoost

# Algorithms Used
1. Linear Regression
2. Ridge Regression
3. Random Forest Classifier
4. Adaboost Regressor
5. XGBoost Regressor

# Data cleaning
There are no null values in the dataset, hence we are good to go ahead with the modeling/ data pre processing

# Data Transformation
1. Prepared a date column from the available year, month, hour, minute columns already present
2. Encode Cloud types into numerical values and later use one hot encoding over these
3. Encode Fill Flag types into numerical values and later use one hot encoding over these

# EDA
1. Checked the distribution plot of the features to gain insights
2. Trying to incorporate Box Cox/ Sq root transformations to convert the Y distributions to normal forms
3. Checking seasonality
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/seasonality.jpg?raw=true)
4. Checking Monthly Trends
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/monthly.jpg?raw=true)
5. Checking Hourly Trends
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/hourly.jpg?raw=true)
6. Checking variation by the week day
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/weeklday.jpg?raw=true)

# Hyper Parameter Tuning
Used gridsearch CV for hyper parameter tuning

# Cross Validation
k fold cross validation, used scoring parameter as f1 (since the false positives were more important) and also looking at class wise f1 scores

# Performance Criteria
Selected the best performing model keeping in mind MSE and R2 scores

# Best Model performance
## For DHI - Random Forest Regressor
### Performance - MSE= 262.04, R2= 92.94%
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/Randomforest_DHI.jpg?raw=true)
## For DNI - Adaboost Regressor
### Performance - MSE= 3225.66, R2= 97.67%
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/Adaboost_DNI.jpg?raw=true)
## For GHI - Random Forest Regressor 
### Performance - MSE= 49, R2= 99.95%
![alt text](https://github.com/sanketmore1234/Sustainability-Machine-Learning-Challenge/blob/main/Randomforest_GHI.jpg?raw=true)
