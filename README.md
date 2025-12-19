# Credit Card Fraud Detection using Machine Learning

## Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques.  
The dataset is highly imbalanced, which makes fraud detection a challenging and realistic classification problem.

The goal is to build an end-to-end data science pipeline, from data exploration to model evaluation, with a strong focus on fraud-related metrics.

## Dataset
- Source: Kaggle – Credit Card Fraud Detection
- Transactions made by European cardholders in September 2013
- 284,807 transactions, with only 492 fraudulent cases
- Features are anonymized using PCA due to confidentiality

## Project Structure
- Data exploration and visualization
- Data preprocessing
- Handling class imbalance
- Model training and comparison
- Model evaluation using ROC-AUC, precision, recall and F1-score

## Models Used
- Logistic Regression (baseline)
- Random Forest (final model)

## Key Results
- Logistic Regression achieved very high recall but low precision for fraud detection
- Random Forest provided a better balance between precision and recall
- ROC-AUC above 0.95 for both models

## Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

## Author
Vanessa Donato  
Data Scientist | Python | Machine Learning
