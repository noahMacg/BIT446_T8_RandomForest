# Grain Storage Purchase Prediction 
**Data Mining Foundations assignment utilizing ML using random forest classification.**

## Overview 
Built a Random Forest classifier to predict customer purchase with 91% accuracy and 92% precision by analyzing 1200 customer records to find factors influencing purchase decisions for business decisions. 

### Technical Stack
Environment: Python 3.10, VS Code, Ubuntu  
Libraries: scikit-learn, pandas, numpy, matplotlib, seaborn 

## Problem and Dataset
**Business problem:** What features are affecting purchase of grain storage bins?

**Data:** 1,200 records with imbalanced dataset (69%  not purchased, 31% purchased). Features included product type, if a grain storage dryer was included, types of warranty,
and volume of bin. 

## Technical Approach
### Method
- Data preprocessing: label encoding, 80/20 random stratified split with a seed.
- Created, fit and tested RF model with hyperparameter tuning.
- Created two parameter optimization loops testing max_samples (200-800) and max_leaf_nodes (3-7)
- Found optimal performance at n_estimators=20, max_samples=200 - reducing overfitting while maintaining accuracy and improving computational efficiency. 

## Results
### Metrics
accuracy:               0.9083  
f-1_score_macro:        0.8840  
f-1_score_micro:        0.9083  
precision:              0.9153  
recall:                 0.7606  
hamming_loss:           0.0917  
jaccard_score:          0.7105  
logloss:                0.2799  
zero_one_loss:          0.0917  
roc_auc_score:          0.9405  
matthews_corrcoef:      0.7748

### Feature Importance
1. Product Type (43.8%) - Primary purchase driver 
2. Warranty Type (34.4%) - Secondary driver 
3. Dryer Availability (12.3%) - Minimal 
4. Storage Capacity (9.4%) - Minimal 

### Business Insight 
- The lift plots showed a range of ~ 2.7-3.6 times more predictive power (lift) than random guessing in the top 30% of customers.
- Cumulative gain showed that we can capture approximately 82% of all potential responders by targeting the top 30% of participants. 
- It will be most beneficial to target marketing efforts to the top 2-3 deciles to gain the most profitable results

*This project shows end-to-end machine learning workflow from a business problem, preprocessing, model building and optimization, and actionable insights for businesses.*


