# Notes on retrieved data

Yelp has hundreds of millions of reviews and millions of consumer interactions with local businesses. Yelp maintains a review filtering system to remove biased or 
fake content from appearing on it, so the data is reliable. Yelp’s fusion API only allows three reviews for a single business, so I decided to web scrape, bypass 
restrictions, and retrieve all the reviews and ratings possible. This folder contains only cleaned data web scraped from Yelp, and the files created to aid my 
classification model development.

# List of raw files

### 1.) [**2.5k_reviews.csv**](https://github.com/JSapun/YelpReviewClassification/blob/main/Data/2.5k_reviews.csv)
This dataset contains 2577 entries on: 
* User reviews
* Star ratings
* Manually classified labels for whether the review is positive or negative (dictated by the number of star reviews)

### 2. [**best_model.pkl**](https://github.com/JSapun/YelpReviewClassification/blob/main/Data/best_model.pkl)
This pickle file contains the final tuned Random Forest Classification model.

### 3. [**w2v_model.pkl**](https://github.com/JSapun/YelpReviewClassification/blob/main/Data/w2v_model.pkl)
This pickle file contains the neural network model used when creating the Word2Vec embeddings for the text reviews. It is needed when preprocessing new data.

### 4. [**stop_words.csv**](https://github.com/JSapun/YelpReviewClassification/blob/main/Data/stop_words.csv)
This file contains a compiled list of NLTK's English stopwords and additional stopwords from the internet. There are 1162 entries.

### 5. [**vectorizedWords.csv**](https://github.com/JSapun/YelpReviewClassification/blob/main/Data/vectorizedWords.csv)
This file contains the mean Word2Vec embeddings vector for each review in the elementary 2.5k_reviews.csv dataset. Each vector is 100-dimensional, thereby producing a 2577x100 CSV.
