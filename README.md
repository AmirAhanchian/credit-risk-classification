# Module 12 Report

## Overview of the Analysis

* In this analysis we were trying to create a machine learning model that could predict high risk vs low      risk loans based on a dataset of historical lending services
* The financial information used in training the models were as follows:
loan_size,	interest_rate,	borrower_income,	debt_to_income_ratio,	num_of_accounts,	derogatory_marks,	total_debt,	loan_status (health vs risky)

* using the data above the model was trained to predict the healtiness of the loan based on the borrower information

* The dataset has large number of healthy loans at about 75K and only 2.5K of risky loans, this mean that the training data is unbalanced and we had to use oversampling methods to correct for this shortcoming of the data set

* We used logistic regression model to first train and test the data, however the accuracy of predictions was not as high as it could be, so we used oversampling to create a new random data set to train the model on and got better results with fitting those into a logistic regression model


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Logistic regression model:
  balanced accuracy = 99.24%
|loan type    |precision|recall|
|Healthy Loans| 1.00    | 1.00 |
|High Risk    | 0.87    | 0.89 |           
|macro avg    | 0.94    | 0.94 |    
|weighted avg | 0.99    | 0.99 |

the precision and recall of the model are perfect for healthy loans however it is short of 90% accuracy for high risk loans which can lead to defaulted loans. the balanced accuracy is misleading as it is very high, due to the fact that the halthy loans pushes the accuracy higher and gives the false pretense of a nearly perfect model. 


* Machine Learning Model 2:
  * Logistic regression model after using resampling on the dataset:
  balanced accuracy = 99.52%
|loan type    |precision|recall|
|Healthy Loans| 1.00    | 1.00 |
|High Risk    | 0.87    | 1.00 |           
|macro avg    | 0.94    | 1.00 |    
|weighted avg | 1.00    | 1.00 |

the precision and recall of the model are perfect for healthy loans. The recall of the model is also perfect for high risk loans which is an imporvment over the first model. The precision however has not changes and stayed at 87%. 
this model is slightly improved over the original model.

## Summary

In the resampled predictions we have a very good predictability, with a great improvment in the High risk predictions as demonstrated by the 100% recall of the model. The f1-score increased by 5% over the original model, the weighted averages in all metrics has gone up to 100% which is an improvment over the first model. 

These improvments however small, can mean the cost to cover falsly approved high risk loans is going to be lower in this model which. This is better for the loaning institution as it means they have a higher profit margin. 

If the finantial institution wants to incur more risk but give more loans out, and that is how the business wants to proceed they could use the first model, however my recommendation is to use model 2. 
