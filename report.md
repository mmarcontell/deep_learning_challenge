# Report on Neural Network Model

## Overview of the Analysis

This analysis was created to leverage an existing dataset in order to predict whether funding applicants would be successful if backed by Alphabet Soup. The dataset used to train the Neural Network consisted of over 34,000 organizations that have recieved funding in the past. The information included in the training data are: application type, affiliation, classification, use case, organization, status, income amount, ask amount, and whether the organization was successful. The data was then binned, converted to categorical data, split, and scaled, before compiling, training, optimizing, and evaluating the model. 

## Results

* Data Preprocessing
  * The target variable used was: IS_SUCCESSFUL
  * The feature variables used were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION,	USE_CASE,	ORGANIZATION,	STATUS,	ASK_AMT, INCOME_LOW, INCOME_HIGH. Income_Low and Income_High were derived from Income_Amt, separated for the sake of optimization.
  * The variables that were dropped for the sake of optimization were: EIN, NAME, and SPECIAL_CONSIDERATIONS



* Compiling, Training, and Evaluating the Model
  * For the first evaluation: I had run the model with 2 hidden layers, with respectively 80 and 30 neurons, using relu as their activation function, and sigmoid for the output layer.
  * After trying to increase the accuracy and optimization, the final evaluation had: 4 hidden layers with 100, 50, 30, and 10 neurons respectively, all activated with relu, with sigmoid as the activation for the output. 
  * My inital evaluation had an accuracy of 71.5%, and by my fourth evaluation it had increased to 73.3%. While an imporvement, this did not meet the goal of 75% accuracy. 
  * The improvement in the performance can be attributed to both the increase in hidden layers and neurons, as well as dropping unnecessary columns from the training data. 

## Summary

By the end of my evaluations, the model was performing at a 73.3% accuracy and 56.15% loss. To improve these results in the future I would reccommend a random forest model instead of deep learning. This would both provide transparancy as to why funding was approved or denied, as well as potentially predicitng at a higher accuracy due to the simplicity of the dataset. 
