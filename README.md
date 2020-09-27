# Insulting-Comment
Here is a project from Kaggle's Contest to decide if a comment is insult or not. 

## Description
The purpose of these project is to create a machine learning system that takes a comment as input and classifies that comment as offensive or non-offensive (neutral). This system will be trained in a set of comments in which the tags (insult or non-insult) are known. In order to measure its effectiveness I used the following classification algorithms: Naive Bayes, SVM, Random Forest.

### Data Set
The data you are given consists of 6,182 comments collected from online forums. They are pre-labeled with values 1 (offensive comments) or 0 (neutral comments). The data set is divided into training set which consists of 2,898 neutral comments and 1,050 offensive comments as well as test set consisting of 1954 neutral comments and 694 offensive.  
In the following examples you can see the two types of comments:  

Insult: "Oh, you are such an idiot ..... you just confirmed that you can not read ... dumb @ rse!"  
Neutral: "You get the gold star! The best post I've seen on here inmonths !! Hilarious ... Great job, Canadian! PS I think we need you to come down here.I'll sponsor you !!   

### Pre-processing and cleaning of data
As a first step you need to convert all characters to lowercase and remove characters such as punctuation, characters such as "\ n", "\ u0111" and generally symbols or urls if there are.  

### Method
You will first use the classic NaiveBayes algorithm for classification (in this step you will convert the comments to word vectors using the sklearn library CountVectorizer sklearn.feature_extraction.text.CountVectorizer - scikit-learn 0.23.1 documentation).  

You will optimize Naivebayes:  
1. with lemmatization  
2. by removing stopwords  
3. by using bigrams  
4. by using Laplace Smoothing

Then you will create a more complex feature table containing part-of-speech features and TF-IDF-based features. You will test all the features you have exported (part-of-speech and TF-IDF) in two additional different models: an SVM and a random decisionforest. In addition, you can experiment with any method/feature you want to achieve the best possible results in the test.

### Summary of features to export
**Part-of-Speech Based Features**: Using the part-of-speech tagger
provided by NTLK, tag each word in each comment with its part of speech (noun, verb, adverb or adjective). Then calculate the percentage of specific tags for each text. That is frequency of each POS tag in each sample, calculated in relation to the total
number of words in the sample. This way you will have 4 new features in
any text, fractionAdverbs, fractionVerbs, fractionAdjectives, fractionNouns. The same
procedure must be done in the test set as well.  
**TF-IDF Based Features**: as you did in the previous tasks

## Note
This python notebook file have the appropriate
results and conclusions of the classification algorithms.  
Performance metrics (i) classification accuracy, (ii) F1 score.



