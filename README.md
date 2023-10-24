# Twitter Airline Sentiment Analysis 🐦

> A natural language processing project that analyzes Twitter sentiment toward major U.S. airlines, classifying tweets as positive or negative using SVM with Count Vectorization, built on the Twitter US Airline Sentiment dataset.

---

## 📌 Overview

Understanding customer sentiment on social media is critical for airlines to monitor brand perception and address service issues. This project analyzes 14,640 tweets directed at six major U.S. airlines, exploring sentiment distribution, negative reason patterns, and temporal trends before building a classification model to predict tweet sentiment.

The project covers end-to-end NLP pipeline including data preprocessing, exploratory data analysis, text cleaning, vectorization, and model evaluation.

---

## 🔍 Key Results

| Model | Accuracy |
|-------|----------|
| SVM (Linear Kernel) | ~91% |

---

## ⚙️ Project Pipeline

### 1. Data Preprocessing
- Converted `tweet_created` column to datetime format
- Dropped columns with over 93% missing values: `tweet_coord`, `airline_sentiment_gold`, `negativereason_gold`
- Retained missing values in `negativereason` to avoid introducing label mismatch
- Dropped neutral sentiment rows to focus on binary classification (positive vs negative)
- Applied Label Encoding on `airline_sentiment` column

### 2. Exploratory Data Analysis
- Sentiment distribution count plots per airline
- Stacked bar chart of sentiment counts by airline
- Negative reason frequency per airline
- Daily negative tweet trend over the 9-day data period (Feb 16 - Feb 25, 2015)
- Word clouds for positive and negative tweets

### 3. Text Cleaning
- Removed non-alphabetic characters using regex
- Converted to lowercase
- Removed English stop words using NLTK

### 4. Vectorization
- Applied **Count Vectorization** on training data
- Transformed both train and test sets into document-term matrices

### 5. Model Training and Evaluation
- Trained **SVM with linear kernel** on vectorized tweet text
- Evaluated using accuracy score, confusion matrix, and classification report

---

## 🛠️ Tools and Libraries

| Tool | Usage |
|------|-------|
| **pandas** | Data loading, cleaning, and manipulation |
| **numpy** | Numerical operations |
| **matplotlib / seaborn** | Data visualization |
| **nltk** | Stop words removal and text preprocessing |
| **wordcloud** | Word cloud generation for positive and negative tweets |
| **scikit-learn** | Count Vectorization, SVM, and evaluation metrics |
| **mlxtend** | Confusion matrix visualization |

---

## 📂 Dataset

This project uses the **Twitter US Airline Sentiment** dataset from Kaggle.

🔗 [View Dataset on Kaggle](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment)
