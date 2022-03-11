# credit-risk-analysis
Module 17: Supervised Machine Learning and Credit Risk

------------------------------

# Overview of Project

This project will use different techniques to train and evaluate models with unbalanced classes, as credit risk is by nature an unbalanced classification problem.


## Project Tasks

The analysis will:

1. Oversample the data using RandomOverSampler and SMOTE algorithms.
2. Undersample the data using ClusterCentroids algorithm. 
3. Combine over- and under- sampling using SMOTEENN algorithm.
4. Compare BalancedRandomForestClassifier and EasyEnsembleClassifer to predict credit risk.


## Resources

-- credit_risk_resampling.ipynb file
-- credit_risk_ensemble.ipynb file

-------------------------------

# Project Results and Summary

Unfortunately, significant errors were encountered when attempting to run these models due to library import issues. 
Alternatively, I have included higher level overviews of benefits and shortcomings of each models in relation to credit risk analysis.

[Ideal goal: Balanced Accuracy Score, Precision + Recall Scores for each model] 

1. RandomOverSampler
Oversamples minority class data relative to majority class data so they can be more easily compared. Does this using random selection. Allows even comparison of small vs. large datasets.

2. SMOTE
Synthetic Minority Oversampling Technique also oversampled minority class data, but uses interpolation. Reduces risk of oversampling compared to random, although still can be strongly affected by outlier data. Especially risky in sensitive situations such as credit worthiness. 

3. ClusterCentroids
Identifies clusters of majority class and generates representative centroids of majority. Majority is then under sampled to match minority class. Does not guarantee more accuracy than Random Undersampling. 

4. SMOTEENN
Combined hybrid approach that oversamples minority and under samples majority classes. This approach can limit risk and increase accuracy over solely under/over sampling. 

5. BalancedRandomForestClassifier 
Allows specific features to be more heavily weighted than others, which can be beneficial in this situation, as indicators such as previous default on a loan should be considered more heavily than whether a person owns or rents a home. 

6. EasyEnsembleClassifier
Selects all samples from minority dataset and only subset from majority class to create more balanced dataset. Also uses boosting. While slow to train, overall can be a very effective approach with less risk than other models. 


