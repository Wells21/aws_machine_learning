# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Wellspring Praise

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realized that the predictions values should not be less than 0, so therefore I made a change to the output of the predictor to ensure that the values are not less than 0.

### What was the top ranked model that performed?
The WeightedEnsemble_L3 model performed the best in all the experiment.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis got an insight into the idea of feature engineering. The insight gotten from the EDA tells us that, adding more features that are statistically significant, or performing feature engineering has a great impact into the models evalutaion (accuracy or whatever evaluation metrics used).

### How much better did your model preform after adding additional features and why do you think that is?
My model before adding additional features had a kaggle score of 1.86412 and after adding additional features reduced drastically to 0.50638. Now checking the hghest ranked user on kaggle, the user has a score of 0.33756. Therefore this tells us how my model performed well after adding additional features. The reason been that adding additional features in the model increased the predictive power, given the model more information on factors that affects the target variable.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I tried just one hyperparameter tuning on my model, and i can say that it improved the kaggle score a little bit, reason been that there are better hyperparamters that would improve the models evalutation.

### If you were given more time with this dataset, where do you think you would spend more time?
I will spend more time in the statistical significant of the variables present, check for multicollinearity that might be affecting the models ability to predict the taget variable accurately.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|n_estimators|max_leaf_nodes|bootstrap|1.86412|
|add_features|max_leaf_nodes|random_state|crterion|0.50368|
|hpo|bootstrap|crterion|num_boost_round|0.49137|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
In Conclusion, in predicting the bike sharing demand using autogloun, I achieved a best kaggle score of 0.49137, with the best model to be the model that was tuned. Also, adding additional features to a data gives the model more chance to have a higher evalutaion on test data (data the model hasn't seen).
