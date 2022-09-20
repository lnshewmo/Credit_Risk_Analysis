# Credit_Risk_Analysis
Using supervised machine learning algorithms to predict credit risk:  

##Overview
 
Purpose: 

Background:


Steps in Machine Learning:
Instantiate model, Fit/Resample, Train, Predict, Evaluate Model Performance

Class imbalance - One class of data is much larger (majority class) than the other class (minority).  This can cause models to be biased toward majority class.  

Strategies to balance the classes by increasing the size of the minority class:
- Random Oversampling: instances from the minority class are randomly resampled
- Synthetic Minority Oversampling Technique (SMOTE): new instances are interpolated from the minority class 

Strategy reduces the size of the majority class to match the minority class:
- Cluster Centroid Undersampling: generates synthetic data points (centroids) which represent clusters in the the data 

Combination strategies:
- SMOTE and Edited Nearest Neighbors (SMOTEENN): first oversamples minority class with SMOTE, then undersamples by dropping datapoints where the 2 nearest neighboring points belong to 2 different classes.

Ensemble strategies:
- Balanced Random Forest Classifier: A collection of decision trees (random forest classifiers) in which each tree is provied a balanced boostrap sample

-Adaptive Boosting (AdaBoost): ensemble technique which trains a sequence of weak models, where each model learns from the errors of the previous model

##Results: 

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Balanced Accuracy Score -
Precision -
Recall -




##Summary: 
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
