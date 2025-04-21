# Credit Card Fraud Detection: An Ensemble Learning Approach
## Overview
This project aims to improve credit card fraud detection by integrating advanced preprocessing techniques and ensemble learning models. Using a combination of data sampling, feature extraction, and hyperparameter optimization, we built a robust classification pipeline capable of identifying fraudulent transactions with near-perfect accuracy.

## Authors
Fateenah Farid, Wahida Shabuddin (Group 10)

## Motivation
Credit card fraud is a growing issue, with global losses projected to surpass $43 billion. Traditional machine learning methods often underperform on highly imbalanced datasets (fraud rate <1%). Our work builds on recent research to improve detection accuracy, address class imbalance, and optimize performance metrics like AUC and AUPRC

## Dataset
* Source: Kaggle - Credit Card Fraud Detection 
* Size: 284,807 transactions
* Features: 30 features (28 PCA-transformed), with one target label (Class)
* Imbalance: Only 0.172% are fraudulent (492 instances)

## Methodology

### Preprocessing
* Sampling Methods: SMOTE, SMOTE-Tomek, RUS
* Feature Extraction: PCA, Convolutional Autoencoder (CAE)

### Model Training
* Algorithms: CatBoost, LightGBM, XGBoost
* Ensemble Method: Soft voting
* Tuning: Bayesian optimization for hyperparameter tuning

### Evaluation Metrics
* Primary: AUPRC, AUC
* Additional: Precision, Recall, F1 Score, Accuracy

### Final Model
* Best Setup: SMOTE-Tomek ➜ CAE ➜ Ensemble (CatBoost, LightGBM, XGBoost)

### Performance
* AUPRC: 0.9997 
* AUC: 0.9998 
* Precision: 0.9946 
* Recall: 0.9932 
* F1 Score: 0.9939 
* Accuracy: 0.9939 

## Key Insights
* CAE outperforms PCA in nonlinear feature extraction
* SMOTE-Tomek outperforms SMOTE and RUS
* Ensemble methods boost robustness and accuracy

## Future Work
* Real-Time Fraud Detection: Test model in a streaming environment (e.g., Kafka, Spark)
* Robust Validation: Use repeated stratified K-Fold cross-validation
* Recent Data Testing: Apply on newer datasets (2020+)

## Application Importance
* Prevent billions in fraud-related losses
* Extendable to other imbalanced domains (e.g., healthcare, insurance)
