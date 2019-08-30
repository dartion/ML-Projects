# Natural Language Processing (NLP)

NLP is an area of computer science and Artificial Intelligence to identify interactions between computer and human languages. In short, it is how to program a computer to process a large amount of data.

In this project, I give a brief programming introduction to tokenizing, speech tagging, chunking and chinking before moving on to classifying text (to identify a review to be positive or negative).

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

In this project, I do the following for the imported text, 

1. Tokenising
	- Sentances 
	- Words 
2. Removing Stop words
	- Remove useless data(words) from a token
3. Stemming words
	- Grouping words based on tenses
	- Normalizing words
4. Use a PunktSentace tokenizer (Trainiable sentence tokenize)
	- Build a function to process_content
	- Identify parts of speech of each word and tokenize them
5. Chunking
	- Using with python regex
	- ChunkGram and chunk parser 
6. Chinking
	- Remove unwanted words from chucked data which are not required.
7. Name Recognition
	- Label different chunks and label them as People place things

## Steps

1. Import NLTK library
2. Download the necessary packages within the NLTK library
3. Test NLTK import by tokenizing sentences and words
4. Introduction to pre-processing
   - Understand how to remove stop words (useless data)
   - Understand how to do stemming of words with NLTK
5. Import sample text from nltk corpus
  - Preprocess the data as per step 4
6. Define a function that will tag each tokenized word with a part of speech
7. Separate words into individual chunks for each sentence using nltk RegexParser and Pase
8. Chinking  = removing unwanted words
9. Use SVM from sklearn to classify the review as "Negative" or "Positive" review based and print the accuracy.


Print the number of documents and get a list of most common words and check how frequently the word happy has appeared in the document.

I then do, **Text Classification** using Linear Support Vector Machine to classify movie review to classify if they get positive or negative reviews based on words.


## Results

Using SVM sklearn classifier, a review is correctly identified as *Negative* with the accuracy of *82.4%*

`SVC Accuracy: 0.824 `




