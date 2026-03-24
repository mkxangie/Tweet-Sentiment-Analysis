# Tweet Sentiment Analysis - Phase 4 Project

## Project Overview

This project builds a multiclass sentiment classifier for tweets about Apple and
Google products. The goal is to automatically classify tweets as positive, negative,
or neutral to help social media and customer experience teams prioritize responses
and track brand perception in real time.

This is a Phase 4 Data Science project using Natural Language Processing (NLP)
techniques including TF-IDF vectorization and text classification.

## Team Members

- Angela Mukami
- Tafford Pessah
- Catherine Nanjala
- Mophat Mwangi

## Project Structure

Tweet-Sentiment-Analysis/
tweet_sentiment_analysis.ipynb    # Main Jupyter notebook
tweet_sentiment_presentation.pptx  # Non-technical presentation
README.md                       # This file

## Dataset

Source: CrowdFlower via data.world

The dataset contains 9,093 human-rated tweets about Apple and Google products,
labeled as positive, negative, neutral, or unclear sentiment.

Download the dataset here:
https://data.world/crowdflower/brands-and-product-emotions

After downloading, rename the file to:
judge-1377884607_tweet_product_company.csv

Place it in the root folder alongside the notebook before running.

## How to Reproduce This Analysis

1. Clone this repository:
   git clone https://github.com/mkxangie/Tweet-Sentiment-Analysis

2. Install the required libraries:
   pip install pandas numpy matplotlib seaborn scikit-learn nltk

3. Download the dataset from the link above and place it in the project folder

4. Open nlp_sentiment_analysis.ipynb in Jupyter Notebook or VS Code

5. Run all cells from top to bottom

## Libraries Used

- pandas - data loading and manipulation
- numpy - numerical operations
- matplotlib and seaborn - data visualization
- scikit-learn - TF-IDF vectorization and all three models
- nltk - stop words for text preprocessing
- re - regular expressions for text cleaning

## Models Compared

| Model               | Accuracy | Weighted F1 |
|---------------------|----------|-------------|
| Naive Bayes         | 0.6468   | 0.5983      |
| Logistic Regression | 0.5401   | 0.5704      |
| Linear SVC          | 0.5998   | 0.6078      |

Linear SVC was selected as the final model based on the highest Weighted F1 score.

## Key Findings

- Linear SVC achieved the best overall balance across all three sentiment classes
- Negative tweets (only 6% of data) were the hardest class to predict
- Class weighting was essential to prevent models from ignoring minority classes
- Top negative signals: doesnt, battery, line ipad, app store
- Top positive signals: cool, great, awesome, fun, smart

## Limitations

- Severe class imbalance with negative tweets at only 6% of the dataset
- TF-IDF cannot capture sarcasm, irony, or sentence context
- Short tweet text and informal language limits preprocessing effectiveness
