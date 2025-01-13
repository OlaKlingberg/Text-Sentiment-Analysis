# Text Sentiment Analysis – Can we beat TextBlob?

## Background
This project was developed for Module 6 of the course *Introduction to Deep Learning* (DTSA-5511) at University of Colorado Boulder.

## Description
The project aims to build a text-sentiment analysis model that outperforms TextBlob’s pre-trained sentiment analyzer, when trained and tested on reviews from Amazon, IMDB, and Yelp.

## Data
* The project makes use of two datasets:
  * [Sentiment Labelled Sentences](https://archive.ics.uci.edu/dataset/331/sentiment+labelled+sentences), housed by UC Irvine Machine Learning Repository. This dataset was used for training and evaluation (after being properly split into training and test sets).
  * Amazon reviews Clothing, Shoes, and Jewelry, which can be accessed from the GitHub repository [Amazon Reviews'23](https://amazon-reviews-2023.github.io/). This detaset was used as a second test set.

## Key Features:
* **Data Preprocessing**: Cleans and prepares text data for analysis, including tokenization, stop-word removal, and lemmatization.
* **Model Development**: Explores three different kinds of models: **Long Short-Term Memory (LSTM), Convolutional Neural Network (CNN)**, and **DistilBERT**.
* **Performance Evaluation**: Compares the accuracy of the explored models against that of TextBlob’s sentiment analyzer.

## Results
The best-performing model was DistilBERT (Run 10 below), which handily beat TextBlob (Run 2) on both the two test sets used.

![image](https://github.com/user-attachments/assets/c2715030-f158-4824-8f60-999e0810130e)

## Conclusion
While the DistilBERT model beat TextBlob's sentiment analyzer on both test sets, on should remember that TextBlob is a ready-made tool that can be applied to any texts. My DistilBERT model, on the other hand, had the benefit of being evaluated on reviews very similar to those that it was trained on. If we took the DistilBERT model that was trained on this dataset and tested it on some ofther kind of texts, such as tweets or newspaper articles, it's likely that it would do worse. For TextBlob, on the other hand, there is no reason to think that it would necessarily perform worse on any other data than it did on these reviews. So TextBlob is still in business.

What can be said though, is that if you want to perform sentiment analysis on a set of some specific kind of texts and have access to (or have the resources to generate) a large enough number of labeled samples, then it's quite likely that you can train a DistilBERT model that will outperform TextBlob on that particular kind of texts.

