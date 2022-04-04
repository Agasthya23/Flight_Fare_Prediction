# Flight_Fare_Prediction

## Table of Content
  * [Overview](#overview)
  * [Codes and Resources Used](#Codes-and-Resources-Used)
  * [EDA](#EDA)
  * [Feature Selection] (#Feature-Selection)
  * [Model Selection] (#Model-Selection)
  * [Model Deployment] (#Model-Deployment)
  * [Deployement on Heroku](#deployement-on-heroku)
  * [Future Scope](#Future-Scope)
 
## Overview
* Built a Flight_Fare_Prediction app that predicts the flight fare tickets that is useful for users while booking flight tickets.
* Implemented Random forest regressor model to the data and hyper tuned using RandomSearchCV to produce the best result.
* Also, built an API using Flask.
* Deployed it on Heroku

Link: [https://flight-fare-prediction-api27.herokuapp.com/](https://flight-fare-prediction-api27.herokuapp.com/)

![Front end](https://imgur.com/N5PReqb)

## Codes and Resources Used

* Python Version: 3.6
* Packages: pandas, numpy, sklearn, matplotlib, seaborn, flask, json, pickle
* For Web Framework Requirements: pip install -r requirements.txt
* Dataset: https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh
* Flask Productionization: https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2

## EDA

* Created separate columns for Departure and Arrival Hour and Minute from Dep_time and Arrival Time
* Similarly, created separate columns Duration_Hour and Duration_Min from Duration_time
* Removed ambiguity by replacing Delhi to New_Delhi in Soure and destination column
* Handled Null values
* Implemented one hot encoding

## Feature Selection
* Dropped Route Column, as it is similar to Total_stops column
* Plotted heatmap and found all the other columns were important

## Model Selection
* Fitted the model and calculated RMSE values
RMSE of LogisticRegression : 4241.59847391815

RMSE of Lasso :  3098.0857737864494

RMSE of Ridge :  3054.3079944116116

RMSE of KNeighborsRegressor :  3194.239775771275

RMSE of DecisionTreeRegressor :  1990.4228022472819

RMSE of RandomForestRegressor :  1625.79627755424

RMSE of GradientBoostingRegressor :  2166.371351829882

RMSE of XGBRegressor :  2203.5048540365233

* RandomForest Regressor performed well with RMSE value of 1625.79
* After Hyperparameter Tuning, RMSE value decrease to 1617.282605100485


## Model Deployment
* Built a  flask API endpoint that was hosted on a local webserver using Flask.
* After taking necessary input from the user returns the Flight Price.

## Future Scope

* Use multiple Algorithms
* Optimize Flask app.py
* Front-End 






