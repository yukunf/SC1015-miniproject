#SC1015 Project
---

##Overview
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


##Dataset
---
The dataset used can be found [here](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction). It has approximately one thousand data points after removing duplicates, and data points are labelled as either having heart disease or no heart disease.

##Methodology
---
**Data Cleaning**

**Baseline Model - Binary Classification Tree**

The binary classification model is used to demonstrate that this task of heart disease detection requires a more complex model, as the binary classification tree yieleded results that were not up to our expections.

**Random Forest model**

We used three different variations of a random forest model to try and model our data. First, we modelled the cleaned data the same way that we had done with our binary classification tree. 
Second, we upsampled the female data as there was a gender disparity noted in our data, and existing literature showed that men are predisposed to have higher rates of heart disease.
Third, we split the female data from the male data and tried to model them seperately with 2 different random forest.

**Support Vector Machine (SVM) model**

**Grid Search**
After finding our best performing model (Random Forest). We used GridSearch to perform hyperparameterisation of our model to try and create an even more accurate model.

##Results
----


