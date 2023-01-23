# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Bhujith Madav V

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Some of the predictions were negative. So I changed the negative values to zero.

### What was the top ranked model that performed?
Weighted ensemble model is the best performing model for this particular dataset

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The problem statement was to predict bikes demand and one of the most important factors is time. For example on all days morning and evening hours would see more demand whereas on saturday's and sunday's demand would be more in nights. Hence splitting the datetime into day, hour and month could contribute more to predictions made by the model.

### How much better did your model perform after adding additional features and why do you think that is?
Performance of the model improved significantly after adding additional features. This was because the added features were more direct in helping the model make predictions.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
In my case I changed few hyperparameter values but it didn't improve model performance compared with feature engineered model performance.

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time on feature engineering.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|num_bag_folds=0|num_stack_levels=0|?|1.80|
|add_features|num_bag_folds=0|num_stack_levels=0|?|0.67|
|hpo|num_bag_folds=5|num_stack_levels=1|?|0.68|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.


![images/model_training_scores.png]

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![images/model_test_score.png]

## Summary
In this project I got to know more about autogluon and how to perform hyper parameter tuning in autogluon. I also learnt how feature engineering can help in improving prediction accuracy.
