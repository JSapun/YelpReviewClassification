# Classifying Great Barrington Restaurant Reviews
Poor customer experience can significantly impact a business—just one negative review can deter potential customers and adversely affect search results. A recent study conducted by Harvard Business School revealed that restaurants experience an increase in business following favorable reviews on Yelp.com [1](https://hbswk.hbs.edu/item/reviews-reputation-and-revenue-the-case-of-yelp-com). This trend highlights the significant impact of online ratings on a restaurant's success. Businesses need insight into how customers feel about their experience, which can help them stay competitive in the local market. The primary motivation behind this initiative is to empower restaurant owners with the ability to quickly identify and address negative feedback, thereby enhancing the dining experience. This project introduces sentiment analysis paired with a classification model to analyze restaurant reviews in Great Barrington.

### Objective
As the project is in the restaurant domain, the business objective of this project is to increase restaurant revenue. Besides correcting the issue and responding to the review, there is not much else the business can do after receiving a negative review. This project serves to aid the long-term revenue goals by revealing poor customer experiences.

### Dataset (Source of data)
Please reference the file descriptions in the [Data](https://github.com/JSapun/YelpReviewClassification/tree/main/Data) subdirectory.
Provide details about the dataset used in the project. Include information such as where the data comes from, its format (e.g., CSV, Excel), size, and any preprocessing steps performed on it. If applicable, mention any data collection methods or sources.

### Target
The outcome of interest is the sentiment of each review in the dataset. I am trying to classify each review as negative or positive (0 or 1). 

### Expected Outcomes

* Main Class (e.g., Negative Reviews (0):
  * Expected Precision: 60%
  * Expected Recall: 98%
* Minor Class (e.g., Positive Reviews (1)):
  * Expected Precision: 99%
  * Expected Recall: 74%

### Evaluation
  * Higher recall is better as the model would rather classify a review as negative than positive
  * Although the precision for class 0 (negative) is unusually low, this could be due to the model performing better than my manual classification method. This goes to show that model performance dictated by ordinary statistics may not be ideal for this scenario as the model is performing exactly as intended. Example: “Sorry to say that I cannot give this place more stars, but I have dined there many times and typically have been quite pleased. This last time was a disappointment…”. This was labeled as a positive review because it had four stars, but my model classified it as negative.
  * The area under the ROC curve (0.91) shows the model can reliably distinguish between positive and negative classes.
  * With increasing customer engagement in Great Barrington, this model would serve restaurant owners well to quickly determine a customer’s experience across all social platforms.

# GitHub Structure:
```
├── Code
  ├── [source files]
├── Data
  ├── [data files]
├── Results
  ├── [figure files]
├── requirements.txt
├── README.md
└── LICENSE
```

# Instructions

### Setup:
* Assuming you have Python 3.12 installed and added to Path, create a virtual env using venv with Windows CMD:
  * Create: ```py -3.12 -m venv venv```
  * Navigating to: ```./venv/Scripts/``` 
  * Enter: ```activate.bat```
  * Navigate back to root: ```cd ../../```
  * Install required packages: ```pip install -r /path/to/requirements.txt```

### Testing the model:
You can easily test the model using the sample code provided in [05_testPKL.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/05_testPKL.ipynb). Below are the steps explained.
#### 1.) Imports
First, you will need to load the Classifer model, the Word2Vec model, a dataframe of text reviews, and a list of stopwords. 
#### 2.) Preprocessing
The model will use 100 'features' to predict the target variable. As we are using a neural network using Word2Vec embeddings, we obtain the average vector displacement for each review. Then you will need to preprocess the reviews by converting them to lowercase, removing punctuation, tokenizing them, and removing stopwords, before joining them back into a string.  
#### 3.) Vectorizing
The next step will require you to split each review into a list of words, obtain the word vector for each word in the review, and take the average of all the word vectors for each review.
#### 4.) Running the model
Then you can create your X and y, and use the Random Forest model to classify your input review!
