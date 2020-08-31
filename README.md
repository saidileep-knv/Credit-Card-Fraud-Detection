# Credit-Crad-Fraud-Detection

It is important to recognize fraudulent credit card transactions, so that the credit card companies do not overcharge customers for items that they did not purchase.

## Dataset

The dataset can be downloaded from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).

The dataset contains transactions made by credit cards in September 2013 by european cardholders. The data is collected over a 2 day period where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

Due to confidentiality issues, the data that is made public only contains numerical input variables which are a result of a PCA transformation.

- Features V1, V2, V3, ... V28 are the principal components obtained with PCA.

- The only features which have not been transformed with PCA are 'Time' and 'Amount'. 

- Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. 

- Feature 'Amount' is the transaction amount, that can be used for example-dependent cost-sensitive learning. 

- Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

## Evaluation Metric

Since the confusion matrix accuracy does not provide any meaningful information in case of unbalanced classification, the model is evaluated upon estimating the accuracy using the Area Under the Precision Recall Curve.


