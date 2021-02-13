# Flipr-Hackathon 
Participated in Hackathon in the month of September.
# Problem Statement-
The objective of the first part of the problem statement was to predict the Covid Cases of a City on 1st September 2020. 
Data preprocessing
In intial phase to find a correlation between different features and no. of patients we need to deal with the "NaN" values. Since the train dataset available is very less we need to replace "NaN" with most appropriate value for different features rather then just skipping row with "NaN". By using sex-ratio and female population we calculated population 2020, and dropped population 2001 & 2011 by replacing them with average rate of population growth over a year. We considered "H-index", "Toilets available", "No. of hospitals" and "Foreign visitors" as a feature of city type, city population growth, city population 2020 and city sex ratio. Thus making clusters using k-means we replaced "NaN" by average of that particular cluster.
# Data Exploration and Data preprocessing:
By using correlation method in pandas we have concluded that Sex ratio, Median Age, Avg Temp, Water purity and H index are least significantly correlated to Covid Cases and so we have omitted these parameters.
Label and one hot encoding of categorical variables was done before traing the model.
# Data modelling and Hyperparameter tuning:
 Various models were tried and tested using 50-fold cross validation method keeping scoring as "neg rmse". After trying several models Gradient Boosting Regression gave desired results of lower rmse. Then hyperparameter tuning gave the optimal parameter which drastically improved the accuracy. Dimensionality reduction methods were employed to further remove the underired or lower relevant features. Finally the results were stored in y_pred array.
