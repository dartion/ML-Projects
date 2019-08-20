###### ML Projects
# Board Game Prediction Review(BGPR)
A ML project  that utilists a game review data set from [Board Game Geek](https://github.com/ThaWeatherman/scrapers/tree/master/boardgamegeek).
This project uses **Linear Regression Model**  and **Random Forest Generator** algorithm for predicting review rating of given names utilising the 80k rows dataset.


## Development
BGPR project is developed in OSX using Python language with the help of Anaconda Jupyter Notebook.
The results are seen in the Jupyter notebook using print commands. 
## Requirements
| Requirement  |  Version |
|--|--|
| OSX | Sierra+  |
| Python | 3.7+  |
| Anaconda | 4.7.0+  |
| Jupyter Core | 4.5.0+  |

## Algorithms Used
- Linear Regression Model (LRM)
- Random Forest Regression(RF)

## Process  

1. Download the dataset from https://github.com/ThaWeatherman/scrapers/tree/master/boardgamegeek
2. Visualise the current data and its properties
  - Display column names and size of the dataset
  - Display histogram for average_rating column
3. Pre-process the data
  - Remove average_rating values which are equal to 0
4. Display co-relation matrix heat map
    - Remove the following columns after realising the less co-relation
      [bayes_average_rating, average_rating, type, name, id]
5. Split the dataset for **Training, Testing and Validating** the Predictions
6. Use KNN and SVC to predict benign and malignant cells
7. Print the predicted score of each algorithm.


## Results
For a target_rating from a randomly picked row is **8.07**

The average rating we predicting using LR is **8.12**

The average rating we predicting using RFR is **7.91**


Therefore, LR is a good algorithm to use for predicting a game review with the current database.
