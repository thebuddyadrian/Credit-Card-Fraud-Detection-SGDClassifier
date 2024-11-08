# Credit Card Fraud Detection

## Tyren Leong and Adrian Damian 

## Description

This project uses Logistic Regression with Stochastic Gradient Descent (SGD) learning to classify whether a credit card data instance is fraud or not.

Dataset source: https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud

>Features of each data instance include:

>>distance_from_home - the distance from home where the transaction happened

>>distance_from_last_transaction - the distance from last transaction happened

>>ratio_to_median_purchase_price - ratio of purchased price transaction to median purchase price

>>repeat_retailer - is the transaction happened from same retailer

>>used_chip - is the transaction through chip (credit card)

>>used_pin_number - is the transaction happened by using PIN number

>>online_order - is the transaction an online order

>>**fraud - is the transaction fraudulent**


## Steps
The data set is processed by checking for missing values then split into 80% for training and 20% for testing.
The Stochastic Gradient Descent (SGD) model is trained on the training data.
The model is used to predict both training and testing data.
The evaluation metrics for both training and testing data are computed.

## Parameter Vector
[-115.37855321017523, 0.06107153686634237, 0.132354154275682, 4.2147483051070695, 19.560601302421674, -3.4099635526040113, -22.644426651210676, 79.34773250900524]


## Results

|   Metrics  | Accuracy | Sensitivity | Specificity | F1 Score | Log Loss |
| :--------- | :------: | :------: |:------: |:------: |:------: |
| Training   |   0.960955   | 0.712381 | 0.984753  | 0.761236 | 0.478306   |
| Test       |   0.961695    | 0.720537 | 0.984827  | 0.767051 | 0.463332   |

![image](https://github.com/user-attachments/assets/879b1acb-49d4-48aa-b12c-4f9ece02fe41)

## Old Results using Naive Bayes Classifier (NBC)

|   Metrics  | Accuracy | Sensitivity | Specificity | F1 Score | Log Loss |
| :--------- | :------: | :------: |:------: |:------: |:------: |
| Training   |   0.95068   | 0.593299 | 0.9848  | 0.677088 | 0.303561   |
| Test       |   0.949905    | 0.593009 | 0.984516  | 0.676692 | 0.307684   |

![image](https://github.com/user-attachments/assets/879b1acb-49d4-48aa-b12c-4f9ece02fe41)


## Comparison to NBC
Logistic Regression has much better performance than Naive Bayes Classifier on both the test and training data, given the higher Accuracy, Sensitivty, and F1 Scores. This is crucial for fraud detection as it means the Logistic Regression classifier has a lower chance of flagging false positives and negatives. Although Logistic Regression has higher log loss, therefore more error in the probability distribution, this isn't as important in a classification task like fraud detection.