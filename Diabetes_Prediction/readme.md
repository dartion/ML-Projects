
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

**N Nearest Neighbours**
0.7777777777777778

**Gaussian Process**
0.8888888888888888

**Decision Tree**
0.8148148148148148

**Random Forest**
0.5925925925925926

**Neural Net**
0.9259259259259259

**Ada Boost**
0.8518518518518519

**Naive Bayes**
0.9259259259259259

**SVM Linear**
0.9629629629629629

**SVM RBF**
0.7777777777777778

**SVM Sigmoid**
0.4444444444444444
