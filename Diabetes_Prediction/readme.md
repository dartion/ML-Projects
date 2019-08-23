
###### ML Projects  
# Diabetes Predictions for Pima Indian dataset (DP)  
An ML project that utilizes a data set from UCI Machine Learning Repository(previously, removed now) to determine if the given patient has diabetes.  
This project uses **Deep Neural Networks** algorithms for predicting diabetes represented by either 0 or 1 using **Keras Classifier**
 
## Development  
DP project is developed in OSX using Python language with the help of Anaconda Jupyter Notebook.  
The results are seen in the Jupyter notebook using print commands.  
## Requirements  
| Requirement | Version |  
|--|--|  
| OSX | Sierra+ |  
| Python | 3.7+ |  
| Anaconda | 4.7.0+ |  
| Jupyter Core | 4.5.0+ |  
  
## Algorithms  
### Deep Neutral Networks with Grid Search CV - KFold  
  Grid search is a model hyperparameter optimization technique. 
  A default k = 3, was used for cross validation. 
  
## Process  
  
1. Download the Pima Indian Diabetes dataset with 700 patients  
2. Pre-process the data  
- Add column names to each column in the database  
- Glucose, Blood Pressure, Skin thickness, Serum Insulin, BMI must have values, therefore, cannot be zero. To replace the 0 values with NaN and drop the rows  
- Convert the data to numpy array  
3. Normalize the data to have similar values in all the columns  
4. Introduce learning_rate as 0.01 and observe the model summary(Parameters - Total, Trainable, non-trainable)  
5. Introduce batch_size and Epochs to identify best batch_size and epoch  
6. For batch_size = 20 and epoch = 100 try learn_rate= 0.001, 0.001, 0.1 and dropout_rate 0.0, 0.1, 0.2  
7. With the best learn_rate and dropout_rate try-out different activation functions and init functions  
8. Tune the number of neurons in each layer to get the best possible predictions  
9. Print the predictions for X_standardized  
10. Print accuracy report for Y as a base against the predictions of Y  
11. Print Classification report for Y as a base against the predictions of Y  
  
## Results  
Best values for  
1. learn_rate = 0.001  
2. drop_rate = 0.0  
3. batch_size = 20  
4. epochs = 100  
5. activation = 'linear'  
6. init = 'uniform'  
7. neuron_in_layer_1= 16  
8. neuron_in_layer_2 = 2

Accuracy
**0.7806122448979592**

N Nearest Neighbours
0.7777777777777778
              precision    recall  f1-score   support

           0       1.00      0.65      0.79        17
           1       0.62      1.00      0.77        10

    accuracy                               0.78        27
    macro avg          0.81      0.82      0.78        27
    weighted avg       0.86      0.78      0.78        27

Gaussian Process
0.8888888888888888
              precision    recall  f1-score   support

           0       1.00      0.82      0.90        17
           1       0.77      1.00      0.87        10

    accuracy                           0.89        27
   macro avg       0.88      0.91      0.89        27
weighted avg       0.91      0.89      0.89        27

Decision Tree
0.7777777777777778
              precision    recall  f1-score   support

           0       0.92      0.71      0.80        17
           1       0.64      0.90      0.75        10

    accuracy                           0.78        27
   macro avg       0.78      0.80      0.78        27
weighted avg       0.82      0.78      0.78        27

Random Forest
0.48148148148148145
              precision    recall  f1-score   support

           0       0.67      0.35      0.46        17
           1       0.39      0.70      0.50        10

    accuracy                           0.48        27
   macro avg       0.53      0.53      0.48        27
weighted avg       0.56      0.48      0.48        27

Neural Net
0.9259259259259259
              precision    recall  f1-score   support

           0       1.00      0.88      0.94        17
           1       0.83      1.00      0.91        10

    accuracy                           0.93        27
   macro avg       0.92      0.94      0.92        27
weighted avg       0.94      0.93      0.93        27

Ada Boost
0.8518518518518519
              precision    recall  f1-score   support

           0       1.00      0.76      0.87        17
           1       0.71      1.00      0.83        10

    accuracy                           0.85        27
   macro avg       0.86      0.88      0.85        27
weighted avg       0.89      0.85      0.85        27

Naive Bayes
0.9259259259259259
              precision    recall  f1-score   support

           0       1.00      0.88      0.94        17
           1       0.83      1.00      0.91        10

    accuracy                           0.93        27
   macro avg       0.92      0.94      0.92        27
weighted avg       0.94      0.93      0.93        27

SVM Linear
0.9629629629629629
              precision    recall  f1-score   support

           0       1.00      0.94      0.97        17
           1       0.91      1.00      0.95        10

    accuracy                           0.96        27
   macro avg       0.95      0.97      0.96        27
weighted avg       0.97      0.96      0.96        27

SVM RBF
0.7777777777777778
              precision    recall  f1-score   support

           0       1.00      0.65      0.79        17
           1       0.62      1.00      0.77        10

    accuracy                           0.78        27
   macro avg       0.81      0.82      0.78        27
weighted avg       0.86      0.78      0.78        27

SVM Sigmoid
0.4444444444444444
              precision    recall  f1-score   support

           0       1.00      0.12      0.21        17
           1       0.40      1.00      0.57        10

    accuracy                           0.44        27
   macro avg       0.70      0.56      0.39        27
weighted avg       0.78      0.44      0.34        27
