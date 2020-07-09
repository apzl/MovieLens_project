# About MovieLens_project notebook

In this EDA notebook, I tried to get the distribution of ratings from ratings file.

- Kyle Balda, Patty Jenkins, Bill condon etc are popular directors in 2020, 2019.....

And after that tried to get the names of top, 'popular directors' and 'popular production companies'

- Universal pictures, Illumination Entertainment, Dune Entertainment, Warner Bros., DC Entertainment are popular production companies...

Then did some anlysis on word counts in titles and tagline and tried Vectorizers and wordcloud.

# About text classification notebook

As we are willing to work on text generation, I started off with text classification and tried to re-implement the article, link is below..

- https://realpython.com/python-keras-text-classification/

# About Dataset 
Sentiment Labelled Sentences Data Set from the UCI Machine Learning Repository. This data set includes labeled reviews from IMDb, Amazon, and Yelp, Each review is marked with a score of 0 for a negative sentiment or 1 for a positive sentiment.

# Techniques

I tried CountVectorizer and TF-IDF on the given dataset

CountVectorizer takes the approach of bag of words.

This works as follows :

1] Each word inside the document will be separated into tokens.

2] Assigning a weight to each token proportional to the frequency with which it shows up in the document and/or corpora.

3] Creating a document-term matrix with each row representing a document and each column addressing a token.

Example : doc = ['This is Count Vectorizer']

   1st token = 'This'
   2nd token = 'is' and so on....
Then the number of times each token occures in a document is counted in case of CountVectorizer.

There are some words which are insignificant so, we need to remove it. In order to do so, we use TF-IDF,

TF - Term Frequency :

 (How many times a term occures in a document)
 tf(i, j) = n(i, j) / E(n(i, j)
IDF - Inverse Document frequency :

 How common a word is across all documents,
 IDF(w) = log ( N/DF(i) )
 
 # Algorithms 
 
           Classifiers                  Yelp      Amazon       IMDB    

    Logistic(CountVectorizer)           83%         77%         74%    

        Logistic(TF-IDF)                82%         78%         76%    

    XGBoost(CountVectorizer)            77%         71%         69%    

        XGBoost(TF-IDF)                 75%         74%         65%    

    RandomForest(CountVectorizer)       80%         76%         74%
 
     RandomForest(TF-IDF)               73%         75%         71%  
     
 These are the score (accuracy) on the text data.

After trying out this algorithms, I tried Deep learning algorithms as were in the given article.


# We are working on text generation and recommender system and for that we have started with some EDA work and then will move on to techniques like text classification.
