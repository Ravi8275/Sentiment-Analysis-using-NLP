# Sentiment-Analysis-using-NLP
This project/algorithm focuses on developing a sentiment analysis system for social media posts. Using Natural language processing techniques the model segregates the new/future posts into different sentiment categories.The steps performed in the construction of the model is mentioned below

- Pandas library is used to load and read the dataset csv file and to convert it into a data frame for further analysis
- A small data analysis is performed to have a glance at the dataset
- Only features of interest were considered for feature engineering and model construction
- Features like date, time of tweet, and platform have nothing to do with the sentiment type of textual post, these features are ignored
- Here considered only text as a feature sample and sentiment as the target variable
- To feed the textual information to the model it has to be vectorized. Two techniques were used here to complete the task i.e. TFIDF(Term frequency-inverse document frequency) and Bag of Words.
- Reason to consider TFIDF as it reduces the importance of regular words and provides more vector score to rare but important words throughout the corpus
- Tried using a Bag of words as it is a simple technique for vectorization.
- Prior to performing the vectorization the entire dataset is split into train and test dataset using the train test split method from Scikit Learn (also for vectorization techniques and classification models)
- After performing the feature engineering i.e vectorization the vectors of the train text data is fed to the model along with its target variable.
- Naive Bayes Multi classifier is chosen as the classification algorithm for its in-depth segregation capabilities.
- After training the model a similar vectorization is performed to test the data set and fed to the model for prediction.
- Here Accuracy and Confusion matrix from Scikit Learn are used as Evaluation Metrics for the Model.

# Conclusion
- Looking at the Evaluation Metrics and also the model evaluation on new tweets it's clear that the model is able to predict the positive sentimental texts accurately
- But the model suffers From neutral and negative segregation.
- If we look at the number of samples for Negative posts,it's less than both the positive and neutral posts leading to an imbalanced dataset. The number is nearly half of the    neutral postings. This might led to confusion while allocating the type of sentiment to the post.
- This can be handled by balancing the dataset i.e. nearly equal number of samples for each sentiment type.
- Better results can be achieved by acquiring more data samples or atleast a little to balance the dataset.
