# Sentiment Analysis of Amazon Reviews


## Competition Result
https://www.kaggle.com/c/caltech-cs-155-2018

Team: The Magic Conch

Result: Rank 20 with 0.858 test accuracy

## Overview
In this project, we performed sentiment analysis on a bag of words representation of Amazon
review data. The team started by researching more about the general topic and looking into different
possible machine learning classifiers/methods.

### Models and Techniques
We looked into the different classifiers available through scikit learn, as well as neural and
convolution networks using the keras package. We proceeded to tune the parameters and use
different methods of bagging and ensembling to optimize the performance of the best classifiers.
The final validation errors of each was gathered using five fold cross validation.
Here’s a summary of the results:

* In some of the classifiers, there were clear signs of overfitting - the training validation
was high (0.90 - 0.99) but the resulting testing accuracy was much lower (0.7). We
remedied this by implementing various regularization and looking into classifiers that did
not overfit.

* After testing with all of the classifiers, we saw that Logistic Regression models, SVM
models and Neural Networks had the lowest validation error, while Linear Regression
had the worst.

* We further tried to improve test accuracy by bagging/ensembling layers of the best
performing classifiers and generating a prediction with it. This proved to have a
significant effect on the performance, and boosted our test accuracy above the targeted
0.85%.

### Discoveries

One major discovery we made as a team was that, in general, our prediction accuracy was
dictated by the quality of the data. Continued improvements in performance in the top models
became marginal and towards the end we were spending copious amounts of time trying to improve
cross validation scores by as little as 0.1%. However, our research into existing literature implied
that similar sentiment analysis tasks could reach 90% - 95% accuracy depending on the
preprocessing approach. In particular, it seemed that n-gram approaches did well, whereas we were
given our data in a 1-gram format.

Another surprising discovery to us as a group was the power behind statistical prediction
models. Right out of the box, many techniques such as Naive Bayes and Linear Regression were
able to reach 80% accuracy. However, meta-algorithms such as ensembling can further improve the
test accuracy of our models by either reducing bias or variance.
