# Credit Risk Analysis

![Credit Risk](Images/credit-risk.jpg)

## Background

Auto loans, mortgages, student loans, debt consolidation ... these are just a few examples of credit and loans that people are seeking online. Peer-to-peer lending services such as LendingClub or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk, so you have been asked by a client to help them use machine learning techniques to predict credit risk.

For this analysis, I built and evaluated several machine-learning models to predict credit risk using free data from LendingClub. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so I needed to employ different techniques for training and evaluating models with imbalanced classes. I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

---

## Conclusions

---

### Resampling

I used the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample LendingClub data and build and evaluate logistic regression classifiers using the resampled data. The models/algoritms used include: Naive Random Oversampler, SMOTE, Cluster Centroids, and SMOTEENN. 

#### Which model had the best balanced accuracy score?
- The Random Oversampler model had the best balanced accuracy score of 67.4% followed closely by SMOTE at 66.2%. SMOTEENN was then next at 64.3%, and Cluster Centroids the worst at 54.4%.

#### Which model had the best recall score?
- The SMOTE model had the best recall score at 69% and the Clustered Centroids model was the worst again at 42%.

#### Which model had the best geometric mean score?
- The Random Oversampler model had the best geometric mean scores at 67% with SMOTE at 66% and SMOTEENN at 64%. The lowest score again was the Clustered Centroids model at 53%.

---

### Ensemble Learning

I trained and compared two different ensemble classifiers to predict loan risk and evaluate each model; specifically, I used a balanced random forest classifier model and an easy ensemble AdaBoost classifier model.


#### Which model had the best balanced accuracy score?
- The Easy Ensemble AdaBoost Classifier performed significantly better with a 93% balanced accuracy score compared to 68% for the balanced random forest classifier.

#### Which model had the best recall score?
- The Easy Ensemble AdaBoost Classifier had a recall score of 92% for high risk, while the Balanced Random Forest Classifier was just 37% for high risk.

#### Which model had the best geometric mean score?
- Again, the Easy Ensemble AdaBoost Classifier scored significant better at 93% compared to 61% for the Balanced Random Forest Classifier.

#### What are the top three features?
- Total Payment Invoice
- Last Payment Amount
- Total Recieved Principal
- Total Payment

