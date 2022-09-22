# Credit Risk Analysis

#### Using supervised machine learning algorithms to predict credit risk
---

## Overview
 
FastLending, a peer to peer lending service would like to use machine learning to predict credit risk in order to expedite the lending process and more accurately identify high and low risk candidates for loans, lowering default rates.  Six different algorithms, using different strategies for imbalanced data, were instantiated and evaluated for their predictive performance using the following metrics:

**Accuracy Score** - what percentage of predictions are correct

**Confustion Matrix** - a matrix mapping the actual distribution of true and false predictions for high and low risk applicants

**Precision Score** - the rate at which the model correctly predicts a classification (How often is it correct?)

**Recall (Sensitivity)** - the rate at which the model correctly detects a classification (Did it find them all?)

**F1 score (Harmonic Mean)** - a weighted average measuring the balance between precision and sensitivity

### Resources:

- Jupyter Notebook
- Scikit-learn library
- Imbalanced-learn library
- Pandas library
- [loans_data.csv](https://github.com/lnshewmo/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv)

### Definitions:

**Machine Learning process flow**: Instantiate model, Fit/Resample, Train, Predict, Evaluate Model Performance

**Class imbalance** - One class of data is much larger (majority class) than the other class (minority).  This can cause models to be biased toward majority class.  In this case, the low-risk applicants belong to the majority class and the high-rish applicants belong to the minority class.

**Strategies to balance the classes by increasing the size of the minority class (resampling) to match the majority class:**

- (Naive Random) Oversampling: instances from the minority class are randomly resampled 

- Synthetic Minority Oversampling Technique (SMOTE): new instances are interpolated from the minority class 

**Strategy to reduce the size of the majority class to match the minority class:**

- Cluster Centroid Undersampling: generates synthetic data points (centroids) which represent clusters in the the data 

**Combination strategies:**

- SMOTE and Edited Nearest Neighbors (SMOTEENN): begin by oversampling the minority class with SMOTE, then undersample by dropping datapoints where the 2 nearest neighboring points belong to 2 different classes.

**Ensemble strategies:**

- Balanced Random Forest Classifier: A collection of decision trees (random forest classifiers) are trained concurrently in which each tree is provided a balanced boostrap sample

- Adaptive Boosting (AdaBoost): A sequence of weak models are trained consecutively, where each model learns from the errors of the previous model

## Results: 

Table 1: Confusion Matrix Summary for 6 Models

<img src="https://github.com/lnshewmo/Credit_Risk_Analysis/blob/main/cm_summary_table.png" height="300" width="600" >

Table 2: Top 5 Features in Order of Importance from the Balanced Random Forest Classifier Model

<img src="https://github.com/lnshewmo/Credit_Risk_Analysis/blob/main/feature_importances.png" height="250" width="250" >

Table 3: Accuracy and Imbalanced Classification Report Summary for 6 Models

<img src="https://github.com/lnshewmo/Credit_Risk_Analysis/blob/main/summary_table.png" height="250" width="450" >

## Summary: 

With reduction of loan default rates as the objective, increased recall of the model to the minority class (high-risk loans) is the prioritized criteria for selecting an appropriate model.  

Of the 6 models evaluated, the Easy Ensemble (AdaBoost) model shows the greatest recall (92%), least number of false negatives (983), highest accuracy (93%), better precision (9%), and best F1 score.  These figures should be translated to real dollars in revenue and effort and compared to the current protocol for evaluating loan applications to determine if this model is an improvement to the current procedure.  If not, there may be other algorithms or features to include for further testing.
