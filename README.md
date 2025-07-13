# SENTIMENT-ANALYSIS

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : ADITYA KAMTHE

*INTERN ID* : CT06DF2353

*DOMAIN* : DATA ANALYTICS

*DURATION* : 6 WEEKS

*MENTOR* : NEELA SANTOSH

## Sentiment Analysis on Walmart Instagram Captions

# Overview
This project performs Sentiment Analysis on Instagram captions from Walmart’s official account using Natural Language Processing (NLP) techniques. The task was carried out in Google Colab, and the dataset was sourced from Kaggle. The goal was to classify each post’s caption as Positive, Negative, or Neutral based on its sentiment. The project also builds a simple machine learning model to automatically predict sentiment labels using text classification methods.

# Tools & Technologies Used
Platform: Google Colab

Dataset Source: Kaggle (Walmart Instagram data)

Programming Language: Python

# Libraries Used:

pandas, matplotlib, seaborn – for data handling and visualization

nltk, TextBlob – for NLP and sentiment scoring

scikit-learn – for model training and evaluation

# Dataset
File: Instagram data.csv

Key Column Used: Caption (Instagram post content)

The dataset includes Instagram engagement data for Walmart. Only the Caption field was used for sentiment analysis in this project.

# Project Workflow

# 1. Data Loading
The dataset was imported using pandas, and the Caption column was extracted as the main source of textual data.

# 2. Text Cleaning
The captions were cleaned using custom functions and nltk:

Converted to lowercase

Removed URLs, special characters, and extra spaces

Removed stop words (using NLTK’s stopword list)

This preprocessing ensures that the text is in a standard format for further analysis.

# 3. Sentiment Scoring using TextBlob
Each cleaned caption was passed through TextBlob to determine its polarity score:

> 0: Positive

< 0: Negative

= 0: Neutral

The sentiment score was converted into a labeled column (Sentiment) containing three classes: Positive, Negative, and Neutral.

# 4. Data Visualization
A bar plot was created using Seaborn to display the distribution of sentiments across the dataset, helping visualize the emotional tone of Walmart's Instagram content.

# 5. Text Classification (ML Model)
To make the sentiment prediction task more scalable:

The captions were vectorized using CountVectorizer from scikit-learn.

A Multinomial Naive Bayes (MNB) classifier was trained to predict sentiment labels based on word frequencies.

The data was split into training and testing sets (80/20 split).

# 6. Model Evaluation
The trained model’s performance was evaluated using classification_report() which included:

Precision

Recall

F1-score
for each sentiment category.

# Results
The MNB classifier successfully learned to distinguish between positive, negative, and neutral captions.

Visual inspection and classification metrics showed that the model performed reasonably well on unseen data.

Positive sentiment was the most dominant class, followed by neutral, with negative being least frequent.

# Conclusion
This project showcases how text data from social media can be analyzed and classified using basic NLP and machine learning techniques. Using Walmart’s Instagram dataset, we gained valuable insights into content tone and built an automated classifier for sentiment detection. This can be useful for businesses looking to monitor brand perception and improve social media engagement.
