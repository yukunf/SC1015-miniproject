# SC1015 Project
---

## Overview
---
This repository contains the project files for SC1015 mini-project.
With the rates of heart disease increasing at a rapid rate all across the globe, we aim to use different classification models to determine the likelihood of heart disease with attributes associated with heart disease.

Listed are the ipynb files used, which should be viewed in order.

1. EDA and Data cleaning
2. Baseline model- Binary Classification
3. Random Forest Classification with Upsampling of Female data points
4. Random Forest Classification by Gender
5. Support Vector Machine model
6. Grid Search Analysis


## Dataset
---
The dataset used can be found [here](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction). It has approximately one thousand data points after removing duplicates, and data points are labelled as either having heart disease or no heart disease.

## Methodology
---
**Data Cleaning**

**Baseline Model - Binary Classification Tree**

The binary classification model is used to demonstrate that this task of heart disease detection requires a more complex model, as the binary classification tree yieleded results that were not up to our expections.

**Random Forest model**

We used three different variations of a random forest model to try and model our data. First, we modelled the cleaned data the same way that we had done with our binary classification tree. 
Second, we upsampled the female data as there was a gender disparity noted in our data, and existing literature showed that men are predisposed to have higher rates of heart disease.
Third, we split the female data from the male data and tried to model them seperately with 2 different random forest.

**Support Vector Machine (SVM) model**

We used a SVM as a regression model to help predict heart disease with the same predictors as our baseline model.

**Grid Search**

After finding our best performing model (Random Forest). We used GridSearch to perform hyperparameterisation of our model to try and create an even more accurate model. We decided to perform GridSearch on our Untouched Random Forest, as it has one of the highest accuracy and the highest True Positive Rate amongst the models that we had tested. A high True Positive Rate is important as we want our model to be especially accurate in detecting cases where heart disease is present. 

## Results
----
This table denotes various performance statistics for the respective models on the test set.

Model | Accuracy | TPR | TNR
--- | --- | --- | --- 
Binary Classification Tree | 0.842 | 0.821 | 0.871
Untouched Random Forest | 0.842 | 0.877 | 0.782
Random Forest with Upsampling | 0.841 | 0.748 | 0.874
Random Forest with Male and Female Split (Averaged) | 0.824 | 0.691 | 0.811
Support Vector Model (SVM) | 0.842 | 0.811 | 0.821
Untouched Random Forest after grid search | 0.842 | 0.887 | 0.770

After Grid Search, the Untouched Random Forest although keeping the same accuracy score, now has a higher True Postive Rate.

## Conclusion
----
In conclusion, we found that it is possible to classify heart disease with heart disease predictors with relatively high accuracy (>80%), despite the gender being imbalanced. More importantly, the True Positive Rate for the models are relatively high, which signifies that our models can predict a positive case (where heart disease is present) very consistently, which could be used in the real world to help doctors to determine which patients are most likely to have heart disease.

Based on the successes of the Machine Learning models, we can determine that there exists a strong correlation between a heart disease and certain predictors like age and beats per minute.

## Contributors
---
@yukunf - Data Cleaning, EDA, Grid Search, Video

@ElijahLimJC - Decision Tree, Random Forest, SVM, Grid Search, Video

@GuanyuGit - Random Forest, Video, Slides Preperation

## References
---
- https://scikit-learn.org/stable/modules/grid_search.html
- https://scikit-learn.org/stable/modules/svm.html
- https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html
