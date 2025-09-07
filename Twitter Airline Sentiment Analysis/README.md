# ✈️ Twitter Airline Sentiment Analysis

## 📌 Project Overview
Airlines receive constant customer feedback on Twitter — both positive and negative.  
This project performs **sentiment analysis** on tweets about six major U.S. airlines to classify sentiments as **positive**, **neutral**, or **negative**.  
The Airlines are - United, US Airways, American, Southwest, Delta, Virgin America

It demonstrates my ability to:
- Perform **data cleaning** and **NLP preprocessing**
- Apply **TF-IDF feature extraction** for text representation
- Train and evaluate **machine learning models** for classification
- Visualize insights using **Seaborn** and **WordClouds**

---

## 🗂️ Dataset
**Source:** [Twitter US Airline Sentiment Dataset](https://www.kaggle.com/crowdflower/twitter-airline-sentiment)

| Column              | Description |
|---------------------|------------|
| `airline_sentiment` | Sentiment label: positive / neutral / negative |
| `text`              | Tweet text |
| `airline`           | Airline being mentioned |
| `tweet_created`     | Timestamp of the tweet |
| `tweet_id`          | Unique identifier |

- **Rows:** ~15,000  
- **Classes:** 3 sentiments (negative, neutral, positive)

---

## 🧠 Approach

### **1. Data Preprocessing**
- Removed URLs, mentions, hashtags, and special characters.
- Lowercased text and removed English stopwords.
- Created a `clean_text` column for modeling.

### **2. Feature Extraction**
- Applied **TF-IDF Vectorization** to convert text into numerical features.

### **3. Modeling**
- **Logistic Regression** → Best overall performance.
- **Multinomial Naive Bayes** → Lightweight baseline.

### **4. Evaluation Metrics**
- Accuracy, Precision, Recall, F1-score.
- Confusion Matrix to visualize misclassifications.

---

## 🌟 Key Takeaways

- Dominance of negative tweets skews model predictions heavily toward "**negative**" sentiment.
- Neutral and positive tweets are consistently underpredicted across all models.
- SMOTE and class weighting improved results slightly, but model bias remains.
- Among the three:
    - Logistic Regression and XGBoost → Best overall accuracy (64% each).
    - Naive Bayes → Best at predicting neutral tweets but weak overall.
- Macro F1 scores (~30%) indicate poor balance in performance across classes.

---


