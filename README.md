# Grain Storage Purchase Prediction 
**Data Mining Foundations assignment utilizing ML using random forest classification.**

## Overview 
Built a Random Forest classifier to predict customer purchase with 91% accuracy and 92% precision by analyzing 1200 customer records to find factors influencing purchase decisions for business decisions. 

## Problem and Dataset
**Business problem:** What features are affecting purchase of grain storage bins?

**Data:** 1,200 records with imbalanced dataset (69%  not purchased, 29% purchased). Features included product type, if a grain storage dryer was included, types of warranty,
and volume of bin. 

## Technical Approach
### Method
- Data preprocessing: label encoding, 80/20 random stratified split with a seed.
- Created, fit and tested RF model with hyperparameter tuning.
- Created wo loops to test different parameter values of max_sample and max_leaf_nodes to find optimal model performance. 
- Found reducing n_estimators=20 and max_sample=200 had minimal affect on model performance and reduced overfitting and increased computational efficiency respectively. 

