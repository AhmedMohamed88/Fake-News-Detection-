📰 Fake News Detection Project Report (Updated)
1. Introduction
Fake news detection has become a critical challenge in the age of social media. This project aims to build an effective fake news detector using Natural Language Processing (NLP) and machine learning. The dataset contains labeled news articles which are processed and classified as either FAKE or REAL.
2. Dataset Description
The dataset (news.csv) has 7,796 rows and 4 columns:
- `title`: Headline of the news article
- `text`: Full content of the news article
- `label`: Either 'REAL' or 'FAKE'

A new feature called `content` was created by combining `title` and `text`. Labels were encoded as 0 (FAKE) and 1 (REAL).
3. NLP Preprocessing Techniques
To prepare the data for machine learning, the following NLP preprocessing steps were applied:
- Lowercasing all text
- Removing punctuation and numbers
- Removing stopwords (e.g., 'the', 'is')
- Stemming words to their base form using PorterStemmer
- Removing extra whitespace
- Creating a clean `content` field for modeling
4. Data Visualization
Exploratory analysis was conducted including:
- Distribution of FAKE vs REAL labels
- Confusion matrices for each model to visualize performance
5. Feature Extraction
TF-IDF (Term Frequency-Inverse Document Frequency) vectorization was applied to convert the text data into numerical features. Parameters used:
- `stop_words='english'`
- `max_df=0.7`
6. Machine Learning Models
Three classification models were trained and evaluated:
- PassiveAggressiveClassifier
- Multinomial Naive Bayes
- Logistic Regression

Each model was trained on TF-IDF features and evaluated using accuracy, precision, recall, and F1-score.
7. Evaluation & Performance
Each model showed strong performance. The PassiveAggressiveClassifier performed particularly well. Confusion matrices were generated for visual understanding of prediction performance.
8. Model Saving
The best-performing model (PassiveAggressiveClassifier) and the TF-IDF vectorizer were saved using `joblib`:
- `fake_news_model.pkl`
- `tfidf_vectorizer.pkl`
9. Conclusion
This project successfully demonstrated fake news detection using NLP and machine learning. Through text cleaning, feature extraction, and training multiple classifiers, we achieved high accuracy and interpretability. Future improvements may include deep learning (e.g., BERT) or web-based deployment with Flask or Streamlit.
