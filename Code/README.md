# Notes on Code

This folder contains the relevant juptner notebook files to my final Random Forest Classification model development. 
The files are labeled according to the order they are run.

## File Descriptions
* [01_webScraping.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/01_webScraping.ipynb) 
  * Web scrapes data, parses, performs manual classification, and exports a cleaned dataframe csv.
  * Output: Cleaned data (.csv), and 1 table (.png)
* [02_featureEngineering.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/02_featureEngineering.ipynb)
  * Serves to compute a numerical representation of text reviews from the cleaned dataset.
  * Input: Cleaned dataframes (.csv)
  * Output: Vecotrized dataframe (.csv), neural network model (.pkl), and 1 plot (.png)
* [03_compareModels.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/03_compareModels.ipynb)
  * Walkthrough of performing cross validation and comparing various models to determine the best performing model for classification.
  * Input: Cleaned dataframes (.csv)
  * Output: 1 table (.png)
* [04_tuneRF.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/04_tuneRF.ipynb)
  * Tuning the final Random Forest model
  * Input: Cleaned dataframes (.csv)
  * Output: Tuned model (.pkl), and 1 plot (.png)
* [05_testPKL.ipynb](https://github.com/JSapun/YelpReviewClassification/blob/main/Code/05_testPKL.ipynb)
  * Testing and evaluating the final Random Forest classifiation model
  * Input: Cleaned dataframes (.csv) and models (.pkl)
  * Output: 1 table (.png)
