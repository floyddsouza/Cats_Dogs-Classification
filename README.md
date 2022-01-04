# Twitter_hate-speech_recognition

This is a sentiment analysis problem of training the machine in detecting multi-label classificaton: positive, neutral or negative reviews. In this project we will use classic ML as well as DL algorithms such as CNN and LSTM

Steps on completing the project.

1) EDA analysis 
2) It is determined that this is an imbalanced dataset, 93% of the data supports non-hate reviews.
3) We will convert the reviews to TFIDF but first we will clean the data by:
  - aplying lowercase
  - we will use regular expressions to remove urls and symbols with '@'
  - tokenizing the words in each sentence using NLTK's TweetTokenizer
remove stop words
Lemmatizing the words to its root using WordNetLemmatizer
joining the tokenized words back into sentences
Applying TfidfVectorizer on the sentecences with bigram and trigram ngram range.
Used Naive Bayes classifier on the imbalanced vectorized dataset to see how it performs. As predicted performance was bad in precision and recall.
Used SMOTE sampling technique to oversample the minority class
Re-ran the Multinomial Naive Bayes to look for improvements. As predicted oversampling improved precision recall and overall accuracy
Tried other Ensemble techniques like random forest and XGBoost
optimized hyperparameter with random Forest and XGBoost by adding class weith balance to Random Forest and adding regularization to XGBoost
Used GridSearchCV to optimize SVM classifier
Assigned a sentiment score using TextBlob to segment each sentance with polarity and subjectivity
Re-ran ML algorithms to observe for results using the new Textblob feature
Used CNN to perform sentiment analysis, to do this we have to:
determine the total number of words used, the vocabulary size and the max sentence length. Using this we will create our image representation of the training sentences, padding any sentences shorter than the sentence with the maximum length
in our CNN we will regularization such as dropout
We will use LSTM as well as LSTM with GRU to see model performance
