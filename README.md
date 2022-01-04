# Twitter_hate-speech_recognition

This is a sentiment analysis problem of training the machine in detecting multi-label classificaton: positive, neutral or negative reviews. In this project we will use classic ML as well as DL algorithms such as CNN and LSTM

Steps on completing the project.

1) EDA analysis 
2) It is determined that this is an imbalanced dataset, 93% of the data supports non-hate reviews.
3) We will convert the reviews to TFIDF but first we will clean the data by:
  - aplying lowercase
  - we will use regular expressions to remove urls and symbols with '@'
  - tokenizing the words in each sentence using NLTK's TweetTokenizer
  - we will remove all stop words
  - Lemmatizing the words to its root using WordNetLemmatizer
  - Joining the tokenized words back into sentences
  - Applying TfidfVectorizer on the sentecences with bigram and trigram ngram range.and setting vocabulary features to 5000 terms.
4) Using various Logistic regression algorith to train
  - We will optimize the alogrithm by adding class balance, adding reularization and hyperparameter tuning. 
