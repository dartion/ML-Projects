###### ML Projects
# Breast Cancer Detection(BCD)
An ML project that utilises a data set from the UCI Machine Learning Repository to determine if the given patient has malignant cancer cells.
This project uses **Support Vector Machine**  and **K Nearest Neighbour** algorithm for predicting benign and cancer cells in the given data set.

## Development
BCD project is developed in OSX using Python language with the help of Anaconda Jupyter Notebook.
The results are seen in the Jupyter notebook using print commands. 
## Requirements
| Requirement  |  Version |
|--|--|
| OSX | Sierra+  |
| Python | 3.7+  |
| Anaconda | 4.7.0+  |
| Jupyter Core | 4.5.0+  |

## Algorithms
### KNN (K Nearest Neighbours)
K Nearest Neighbour(KNN) is a classification technique.
KNN in simple terms is, in a given dataset to predict the classification of the target chooses K neighbours. 
The classification of the target will be the same classification the majority of its nearest neighbours determined by the variable K.
The value of K could be changed from 1 to n. n is the size of the data set. 

Used KNN because
1. Since it is a classification technique and the output is relatively simple to understand.
2. It takes fewer resources and time for the computations and provides a reliable prediction.
3. Good to use when the dataset is large

### Support Vector Machine
It is a classification algorithm which draws decision boundary looking at the extremes in the data.
Support vectors(lines) are the data points which are close to opposing class.
D+ and D- are the lines closest to positive point and negative point appropriately.
Margin is the distance between D+ and D-.
If the data is non-linear we use a simple function to convert the points into 2 dimensional and then draw the support vectors to classify the data.

Used SVC here because
1. Memory efficient
2. This is a linear dataset


## Process  

1. Download the dataset from UCI Machine Learning Repository
2. Pre-process the data
  - Add column names to each column in the database as
    - clump_thickness, uniform_cell_size, uniform_cell_shape, marginal_adhesion, single_epithelial_size,     bare_nuclei, bland_chromatin, normal_nucleoli, mitosis, class
  - Add 9999 to undefined data in each row-column
3. Describe data to see some basic parameters such as mean, median, percentage of each classification.
4. Produce histogram to check linear relation between each column.
5. Split the dataset for **Training, Testing and Validating** the Predictions
6. Use KNN and SVC to predict benign and malignant cells
7. Print the accuracy of each algorithm for predicting the correct values.


## Results
Results predict if a given cell in the test data set is either
2 = Benign
*OR*
4 = Malignant 

**KNN**
Accuracy = **0.9642857142857143**
                  
                    precision      recall   f1-score   support
           2          0.98          0.97      0.97        95
           4          0.93          0.96      0.95        45
           
    accuracy                                  0.96       140
    macro avg         0.96          0.96      0.96       140
    weighted avg      0.96          0.96      0.96       140

**Support Vector Machines**

Accuracy = **0.9714285714285714**

                    precision     recall   f1-score   support
           2          1.00         0.96      0.98        95
           4          0.92         1.00      0.96        45
           
    accuracy                                 0.97       140
    macro avg         0.96         0.98      0.97       140
    weighted avg      0.97         0.97      0.97       140

For efficient prediction for the type of dataset both KNN and SVM could be used.
