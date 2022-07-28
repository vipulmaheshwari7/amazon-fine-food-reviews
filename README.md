# amazon-fine-food-reviews
Objective
Analyze ~500,000 food reviews from Amazon and determine the polarity on reviews
About this Dataset

Context
This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories

Contents
Reviews.csv: Pulled from the corresponding SQLite table named Reviews in database.sqlite

database.sqlite: Contains the table 'Reviews'

Data includes:

Reviews from Oct 1999 - Oct 2012
568,454 reviews
256,059 users
74,258 products
260 users with > 50 reviews
Table of Contents
Loading the dataset , EDA
Pre-processing the dataset
Text Featurization
Review Text -->Text Vector
Applying different classification model with different hyperparameter
KNN
Naive Bayes
Logistic Regression
conclusion
Output Sample
*********k-fold knn (n_neighbors=k , weights='uniform') *********** ************* using k-fold to find best K-value ******************* best accuracy is 88.97500048734379 on cv datatset using 10 fold at k-value 7 genearalisation accuracy using optimum k-value at k = 7 is 0.8746

1. Loading the Dataset
downloading dataset from kaggle 'amazon fine food reviews' , and use 'panda' library to load the dataset
Exploratary Data Analyses of dataset
understanding the distribution of features
2. Text Preprocessing of dataset
removing duplicate values
removing stopwords
cleaning unnecessary words
remove punctuations and html tags
stemming of words , etc
3. Text Featurization
Using text Featurization techniques to convert text into vector to make it ready to apply classification model

Bow
uni-gram
bi-gram
Tf-Idf
uni-gram
bi-gram
avg W2V
avg Tf-Idf W2v
4. Applying classification model
1. KNN
applying KNN on differnent Text Featurization(bow,tf-idf,avg w2v,avf tf-idf w2v) with optimum hyperparmeter
changing diifernt parameter of KNN to improve accuracy(Brute force , Kd-tree )
evaluate the performance matrics
Accuracy Table
Text Featurisation	Accuracy( % )
BOW	88.48
Tf-Idf	89
avg W2V	89.96
avg Tf-Idf W2v	89.55
Conclusion of KNN
* KNN is a lazy learning algorithm and takes quite a much time
* best generaliztion accuracy of KNN on Amazon fine food reviews is 89.96% using avg w2v vectoriser
* Apply other algorithms which has less latency time and more accuracy
2. Naive Bayes
Applied Naive Bayes using Bernoulli NB and Multinomial NB on Different Text Featurization of Data (bow,tf-idf,avg w2v,avf tf-idf w2v) with optimum hyperparmeter
evaluate performance metrics
Accuracy Table
Text Featurisation	Accuracy (%)
BOW	87.72
Tf-Idf	85.58
avg W2V	86.82
avg Tf-Idf W2v	87.1
Confusion Metric with best algo and optimum hyperparameter 
Conclusion of Naive Bayes
* Naive bayes is faster than KNN but giving less accuracy compared to KNN
* best generaliztion accuracy of Naive bayes on Amazon fine food reviews is 87.72% using avg BOW vectoriser
* Now, we will try logistic regression classification technique on our dataset and 
  check if it is better or not.
3. Logistic Regression
Accuracy Table
Text Featurisation	Accuracy
BOW	92.93
Tf-Idf	92.48
avg W2V	92.30
avg Tf-Idf W2v	91.83
Confusion Metric with best algo and optimum hyperparameter 
Conclusion of Logistic Regresion
* It is seen that logistic regression works better and faster than above model(Knn and Naive Bayes).
* Best generalization accuracy on amazon fine food reviews using logistic regression
    gridsearchCV is 92.93 % on BOW bigram 
* Logistic regression works faster than Knn and naive bayes as its running time complexity 
    is only O(d)
* We can also reduce its time complexity further by increasing sparsity
    (increase lambda=1/c in L1 regulizer)by trading with errors.
* Logistic regression is also very useful in feature interpretable as it uses weights to
    interprate featues.

**NOTE I have trained logistic regression on only 10000 data-points in avg w2v and avg tf-idf
    w2f becouse of time constrain.
