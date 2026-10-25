# Fraud Detection - Business Insights

## Project Overview
This project builds a machine learning model to identify
potentially fraudulent credit card transactions.

## Dataset
- Source: Kaggle Credit Card Fraud Detection
- Original dataset: 284,807 transactions
- Rows removed as exact duplicates: 1,081
- Cleaned dataset: 283,726 transactions
- Fraud cases after cleaning: 473

## Final Model
- Algorithm: Random Forest
- Decision threshold: 0.3200
- Threshold selected using the validation set.
- Final performance evaluated on a separate test set.

## Final Test Results
- Precision (fraud): 0.9286
- Recall (fraud): 0.7324
- F1-score (fraud): 0.8189
- PR-AUC (Average Precision): 0.8111

## Confusion Matrix Counts
- True positives: 52
- False positives: 4
- True negatives: 42484
- False negatives: 19

## Business Interpretation
The model identifies 52 fraudulent transactions in the test set.
It misses 19 fraudulent transactions and flags 4 legitimate
transactions for further review.

A lower threshold may increase fraud detection but can also
increase false alarms. The preferred operating threshold should
reflect the relative cost of missed fraud and manual investigations.

## Limitations
- Results are based on a public, anonymized dataset.
- The test set uses a stratified random split, not a chronological split.
- Model performance does not guarantee equivalent performance
  on real-world banking transactions.
- Model predictions should support, not replace, risk investigation.
