###### ML Projects  
# DNA Classification (DNAC)  
An ML project that utilizes a data set from the UCI Machine Learning Repository to predict a promoter/non-promoter for a given DNA sequence.  
  
This project use KNeighborsClassifier, MLPClassifier, GaussianProcessClassifier, RBF, RandomForestClassifier, AdaBoostClassifier, GaussianNB and SVC  
compare the prediction accuracy of each algorithm.  
  
## Development  
DNAC project is developed in OSX using Python language with the help of Anaconda Jupyter Notebook.  
The results are seen in the Jupyter notebook using print commands.  
## Requirements  
| Requirement | Version |  
|--|--|  
| OSX | Sierra+ |  
| Python | 3.7+ |  
| Anaconda | 4.7.0+ |  
| Jupyter Core | 4.5.0+ |  
  
## Process  
  
Process  
1. Get the DNA classification Promoter dataset from UCI repository  
2. Pull out each character in the sequence columns except '\t' character and append as a column to the dataset  
3. Learn more about the data by describing the data  
4. Switch to numerical Data using pd.get_dummies function  
5. Remove the redundant class column after the previous step  
6. Splitting Training and Validation datasets  
7. Import all the 10 learning algorithms  
8. Configure each algorithm  
9. For each algorithm print Algorithm Name, Mean of the Results, Std of the results for training data set and test dataset
 
## Results  
For the given dataset **SVC linear** algorithm has 96% accuracy.


The result summary of all other algorithms are as follows:
**N Nearest Neighbours
0.7777777777777778**

		              precision    recall  f1-score   support
		              
		       0       1.00      0.65      0.79        17
		       1       0.62      1.00      0.77        10

    accuracy									   0.78        27
    macro avg      	       	   0.81      0.82      0.78        27
    weighted avg       	       0.86      0.78      0.78        27

**Gaussian Process
0.8888888888888888**

		              precision    recall  f1-score   support

	               0       1.00      0.82      0.90        17
	               1       0.77      1.00      0.87        10

		accuracy 	       	                   	   0.89        27
       macro avg       	       0.88      0.91      0.89        27
    weighted avg               0.91      0.89      0.89        27

**Decision Tree
0.7777777777777778**
  
			      precision    recall  f1-score   support

		       0       0.92      0.71      0.80        17
		       1       0.64      0.90      0.75        10

        accuracy			           	   0.78        27
       macro avg   	   0.78      0.80      0.78        27
    weighted avg       0.82      0.78      0.78        27

**Random Forest
0.48148148148148145**

			      precision    recall  f1-score   support

		        0       0.67      0.35      0.46        17
		        1       0.39      0.70      0.50        10

		accuracy                		   		0.48        27
       macro avg    	   	0.53      0.53      0.48        27
    weighted avg           	0.56      0.48      0.48        27

**Neural Net
0.9259259259259259**

			      precision    recall  f1-score   support
	
		        0       1.00      0.88      0.94        17
		        1       0.83      1.00      0.91        10

		accuracy               		            0.93        27
       macro avg       		0.92      0.94      0.92        27
    weighted avg       		0.94      0.93      0.93        27

**Ada Boost
0.8518518518518519**
              
		              precision    recall  f1-score   support

		         0       1.00      0.76      0.87        17
		         1       0.71      1.00      0.83        10

        accuracy                      		     0.85        27
       macro avg      		 0.86      0.88      0.85        27
    weighted avg       	   	 0.89      0.85      0.85        27

**Naive Bayes
0.9259259259259259**
	              
		              precision    recall  f1-score   support

		         0       1.00      0.88      0.94        17
		         1       0.83      1.00      0.91        10

		accuracy         	                     0.93        27
       macro avg       		 0.92      0.94      0.92        27
    weighted avg       		 0.94      0.93      0.93        27

**SVM Linear
0.9629629629629629**
              
		              precision    recall  f1-score   support

		         0       1.00      0.94      0.97        17
		         1       0.91      1.00      0.95        10

		accuracy           	                     0.96        27
       macro avg       		 0.95      0.97      0.96        27
    weighted avg       		 0.97      0.96      0.96        27

**SVM RBF
0.7777777777777778**
              
		              precision    recall  f1-score   support

		         0       1.00      0.65      0.79        17
		         1       0.62      1.00      0.77        10

		accuracy         	                     0.78        27
       macro avg       		 0.81      0.82      0.78        27
    weighted avg       	 	 0.86      0.78      0.78        27

**SVM Sigmoid
0.4444444444444444**
              
		              precision    recall  f1-score   support

		          0       1.00      0.12      0.21        17
		          1       0.40      1.00      0.57        10

		accuracy                           	      0.44        27
       macro avg       		  0.70      0.56      0.39        27
    weighted avg       		  0.78      0.44      0.34        27
