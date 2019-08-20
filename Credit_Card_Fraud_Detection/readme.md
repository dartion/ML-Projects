###### ML Projects
# Credit Card Fraud Detection(CCFD)
A ML project  that utilists a kaggle [dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud).

This project uses **Local Outlier Factor **  and **Isolation Forest** algorithms for predicting fraudulent cases in the dataset.

## Development
CCFD project is developed in OSX using Python language with the help of Anaconda Jupyter Notebook.
The results are seen in the Jupyter notebook using print commands. 
## Requirements
| Requirement  |  Version |
|--|--|
| OSX | Sierra+  |
| Python | 3.7+  |
| Anaconda | 4.7.0+  |
| Jupyter Core | 4.5.0+  |

## Algorithims 
#### Local Outlier Factor
  This method is an unsupervised outlier detection metho which calculates anomaly scores of each sample and that we call  Oultlier factor. It measures the local deviation of the density of a given sample wrt to its neighbours. 
  Its local and the anomaly score depends on how isolated the object is with respect to the surrounding neighbourhood.
  This is going to be determined in the same way as the KNN(K Nearest Neighbour) method. However, we are calculating the anamoly score based on off the neighbours.
  
#### Isolation Forest Algorithm
 RF is going to return an anomaly score of each sample in the given dataset. It isolates the observation by randomly selecting a feature and randomly selecting a split value between the maximum and minimum values of the selected feature.
 All columns are considered a feature when using this method.
 Recursive partitioning can be represented by a tree structure, the number of splittings required to isolate a sample is equivalent to path length from the root node to the terminating node.
 The path length is averaged over random trees and is a measure of normality and a decision function.
 Random partitioning produces noticeably shorter paths for anomalies. Hence, when a forest of random trees collectively produces shorter path lengths for a particular sample, they are highly likely to be anomalies.
 This is a combination of random forest algorithms and is going to isolate points which have shorter path lengths or more likely to be anomalies.


## Process  

1. Download the dataset from Kaggle
2. Identify the fraudulent cases by visualising the data
3. Consider values of class **0** as valid case and **1** as a fraud case
4. To utilise less computation resource, get around 10% of the dataset for testing, training and validating
5. Visualise the current data and its properties
  - Display column names and size of the dataset
  - Display histogram for every column
  - Display a correlation matrix heat map
6. Pre-process the data
  - Remove columns with irrelevant values
7. Use the Local Outlier Factor and Isolation Forest Algorithm to predict if a given transaction is fraudulent.
7. Print the predicted results of each algorithm


## Results
Name: **Isolation Forest**
No. of Error: **71** 
Accuracy Score: **0.99750711000316**
Classification Report

                    precision    recall  f1-score   support
               0       1.00      1.00      1.00     28432
               1       0.28      0.29      0.28        49
    accuracy                               1.00     28481
    macro avg          0.64      0.64      0.64     28481
    weighted avg       1.00      1.00      1.00     28481

Name: **Local Outlier Factor**
No. of Error: **97** 
Accuracy Score: **0.9965942207085425**
Classification Report


                  precision    recall  f1-score   support

                0       1.00      1.00      1.00     28432
                1       0.02      0.02      0.02        49
    accuracy                                1.00     28481
    macro avg           0.51      0.51      0.51     28481
    weighted avg        1.00      1.00      1.00     28481


`Local Outlier Factor` has **97** total errors which are relatively high.
Although, **99.65%** accurate.
Precision, for valid cases, had the precision of 100%, for fraud cases, we had only 0.02. i.e we have very few fraudulent cases labelled as fraudulent.
Note: Precision also counts for false positives which were assigning a bunch of valid credit transactions as positive.

`Isolation Forest` has **71** errors and **99.75** accuracy.
Prec is **30%** better than **0.02** (Although we are identifying only 30 fraudulent cases)

For this scenario, **Random Forest method** is better compared to Local outlier factor. 
However, the results could be improved if the dataset is completely utilised(although computationally expensive)




