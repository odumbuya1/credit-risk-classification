# Creit_RisK_Report

Credit Risk Report:


Purpose of Analysis
The objective of the analysis was to determine the predictive power of the logistic regression model between loans claassified as '0' for healthy loans and '1' for high risk loans using original dataset. 

The Dataset:
The dataset includes columns loan size, interest rate, income of borrowers, debt to income ratio,number of accounts, derogatory remarks, loan status and total debt. The model was trained to predit loan ststus, classified into `0` (healthy loan) and `1` (high-risk loan) labels?

Stages of the machine learning process:
 Data preparation: import csv file into pandas dataframe and review dataframe; use train_test_split method () from sklearn model selection to split data into train and test sets; identified y label and x features sets; fit the logistic regression model; test the trained and fitted model to prdict values of y using (x test) data

Result
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384


The classification report above provides the required metrices to eveluate the model's performance using the precision and recall metrices and the overall perforamce via balanced accuracy index i.e. macro avg. The logistic regression model classified "loan status" into the two following classes; '0' = healthy loan and '1' = high risk loan ads seen above.

Class `0` (healthy loan):
the model reports a precision ratio of 1/1 or 1.00 - Out of the total predicted healthy loans observations, the model correctly predicted all observations with excellent ratio of 1/1 =1 or 100% precision. 

While for the class of high risk loan `1` -  the model's precion ratio dropped to 0.85. This means given all predicted observations for high risk loans the model was only able to predict 85 percent as high risk while a remainder 15 percent was not captured by the model. That will be accounted for slippages in model proficiency. 

Recall metric:
To me the recall metric is the most superior or true reflection of model performance. The reason being, the reall ratio measures the proportion of correctly predicted observations relative to the actual observations y, i.e. y_actual. In this regard, in the class `0` (healthy loan) displayed above, a recall ratio registered 0.99. This means the variation between the model prediction and actual values was 0.01 = 1%. The model predicted health loan with very high accuracy.

On the other hand, the model was able to correctly predict 91% of all high risk loans, which means 9% of high risk loans was  not captured by model and where actually in the high risk category.

The Overall true performance of the model is indicated by macro avg of 0.95 recall. This metric is also known as the balanced accuracy ratio. It is the avearge of both recall ratio for the healthy loan and high risk loans (0.99 + 0.91)/2 = 0.95

Nevertheless, the model's predictive power for high risk loans should be improved upon. 
