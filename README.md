# Credit_Risk_Analysis

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. With such incredible growth, FinTech firms are storming ahead of traditional loan processes. We'll need to employ different tenchnique to train and evaluate models with unbalanced classes, using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. By using the latest machine learning techniques, these FinTech firms can continuously analyze large amounts of data and predict trends to optimize lending.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Each algotirhm will fit in logistic regression to evaulate the balanced accuracy score, generate the confusion matrix and classication report.

## Results
Each Algorithms below fit in Logistic Regression model to train

1. Resampling Models Oversampling RandomOverSampler algorithms:

* balanced accuracy scores = 0.62499
* precision scores for high_risk = 0.01, low_risk = 1.00
* recall scores for high_risk = 0.60, low_risk = 0.65
![Resampling_confusion matrix](https://user-images.githubusercontent.com/100484606/178210048-562c2f64-2d16-4f5b-9b5c-e3e11d18d764.JPG)


2. Resampling Models Synthetic Minority Oversampling Technique(SMOTE) algorithm:

* balanced accuracy scores = 0.65125
* precision scores for high_risk = 0.01, low_risk = 1.00
* recall scores for high_risk = 0.64, low_risk = 0.66
![SMOTE_Oversampling](https://user-images.githubusercontent.com/100484606/178209676-e601a4df-a5fb-4ccf-ae42-93ac059d43bc.JPG)


3. Resampling Models Undersampling ClusterCentroids algorithms:

* balanced accuracy scores = 0.51338
* precision scores for high_risk = 0.01, low_risk = 1.00
* recall scores for high_risk = 0.56, low_risk = 0.46
![SMOTEEN_Undersampling](https://user-images.githubusercontent.com/100484606/178209769-b54c102c-f7e0-4b84-8daa-7ba9df4ffd79.JPG)

4. Combinatorial approach of over- and undersampling SMOTEENN algorithms:

* balanced accuracy scores = 0.61635
* precision scores for high_risk = 0.01, low_risk = 1.00
* recall scores for high_risk = 0.69, low_risk = 0.54
![Combination_Sampling](https://user-images.githubusercontent.com/100484606/178209429-aa56a895-e5ac-43a6-88b9-6566eb4a8b9c.JPG)

5. Ensemble Classifiers Balanced Random Forest Classifier algorithms:

* balanced accuracy scores = 0.78712
* precision scores for high_risk = 0.04, low_risk = 1.00
* recall scores for high_risk = 0.67, low_risk = 0.91
![Ensemble_BalanceRandomForest](https://user-images.githubusercontent.com/100484606/179457335-031f233f-f83f-4546-ac15-cb4d88b465af.JPG)


6. Ensemble Classifiers EasyEnsembleClassifier algorithms:

* balanced accuracy scores = 0.9255
* precision scores for high_risk = 0.07, low_risk = 1.00
* recall scores for high_risk = 0.91, low_risk = 0.94
![Ensemble_EasyEnsembleClassifier](https://user-images.githubusercontent.com/100484606/179457298-31acb7e5-5866-4eb8-b803-f731001bf51d.JPG)


## Summary
As the result, we run through all 6 machine learning models, the highest balanced accuracy scores is the Easy Ensemble Classifier algorithms, which gives us 0.9255 high score of accuracy. On the other hand the precision score that correctly predicted the high risk loan is 0.07, low risk loan is 1.00, the recall(sensitive) scores that correctly detect potential high rick loan is 0.91, low risk loan is 0.94.

Based on that result, Easy Ensemble Classifier algorithms machine learning models would be recommended to use. Although all 6 machine learning models can correctly predict the low credit risk loan, EasyEnsembleClassifier got the highest score overall at 0.07. In conclusion, above the 90% of the current analysis, utlizing EasyEnsembleClassifier will perform a High-Risk loan precision as a great value for the overall analysis.
