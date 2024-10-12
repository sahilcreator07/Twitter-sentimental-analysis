**Sentiment140 dataset with 1.6 million tweets**

dataset link :- https://www.kaggle.com/datasets/kazanova/sentiment140

Twitter Sentiment Analysis
This project focuses on sentiment analysis using the Sentiment140 dataset. The goal is to build a logistic regression model to classify tweets as positive or negative based on the sentiment expressed in the text. The project involves data preprocessing, feature extraction, model training, and evaluation.

Table of Contents
Dataset
Installation
Project Workflow
Results
Model Accuracy
Usage
References
Dataset
Sentiment140 dataset with 1.6 million tweets
Dataset Link

About the Dataset:
Context:
This dataset contains 1,600,000 tweets extracted using the Twitter API. It has been annotated for sentiment detection with the following labels:
0 = Negative
4 = Positive
Content and Fields:
target: Polarity of the tweet (0 = negative, 2 = neutral, 4 = positive)
ids: Tweet ID (e.g., 2087)
date: Date and time of the tweet (e.g., Sat May 16 23:58:44 UTC 2009)
flag: The query used to extract the tweet (e.g., "lyx"). If there’s no query, it is NO_QUERY.
user: Username of the person who tweeted (e.g., robotickilldozr)
text: The actual content of the tweet (e.g., "Lyx is cool")
Installation
Requirements
Make sure you have the following libraries installed:

pip install pandas numpy scikit-learn matplotlib seaborn wordcloud nltk pickle-mixin
You also need to download the Sentiment140 dataset from Kaggle:

!kaggle datasets download -d kazanova/sentiment140
Project Workflow
Data Loading and Preprocessing:

Extract the data from the ZIP file.
Assign proper column names to the dataset.
Replace positive labels from 4 to 1 and drop neutral tweets (2) to simplify the problem as binary classification.
Clean the text: Remove stopwords, special characters, URLs, and numbers.
Apply stemming to reduce words to their root form.
Feature Extraction:

Use TF-IDF Vectorizer to convert the text into numerical features.
Train-Test Split:

Split the dataset into 80% training and 20% test sets.
Model Building:

Train a Logistic Regression model using the training data.
Evaluation:

Evaluate the model’s performance on both training and test datasets using accuracy scores.
Results
Training Accuracy: 79.8%
Test Accuracy: 77.8%
Sentiment Distribution
Below is a visualization of sentiment distribution within the dataset:

