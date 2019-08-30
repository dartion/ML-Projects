Object Recognition(OR)

We load CIFAR Dataset from Canadian Institutre with about 60k images and build a CNN to predict a given image is one of the 9 classes
i.e ['aeroplane', 'automobile', 'bird', 'cat', 'dog', 'frog', 'horse', 'ship', 'truck'].


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
  

## Process

1. Import the 60k images from cifar10
2. Split the dataset into training and testing dataset
3. Print the shape of the testing and training dataset
4. Build a grid of 3x3 images of 32x32 pixels each
5. Preprocess the data
	- Normalise the test and train data
6. Build a CNN
	- Add convilutional layers as follows
7. Define Hyper parameters
8. Define optimizer and compile the model and print the models summary
9. Fit the model if you have GPU(As it takes really long time to complete....)
10. Test the model with the pretrained weights
11. Make a dict for class labels and names 
12. Generate batch of 9 images to predict
13. Make Predictions and display them with Actual and Predicted pictures.


Download free trained weights (hdf5 works with Keras)
https://github.com/PAN001/All-CNN/blob/master/all_cnn_weights_0.9088_0.4994.hdf5


## Results 


