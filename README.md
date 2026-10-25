# Credit Card Fraud Detection

A machine learning portfolio project for identifying potentially
fraudulent credit card transactions using Random Forest.

## Business Problem

Fraudulent transactions are rare compared with legitimate transactions.
A useful detection system must evaluate fraud precision and recall,
rather than relying on accuracy alone.

## Dataset

- Source: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Original records: 284,807
- Records after exact-duplicate removal: 283,726
- Fraud cases after cleaning: 473

The raw dataset is not included in this repository. Download it from
Kaggle and follow the notebook's data-loading instructions.

## Methodology

1. Data inspection and exploratory data analysis.
2. Duplicate inspection and data cleaning.
3. Stratified train, validation, and test split.
4. Baseline comparison: Logistic Regression and Random Forest.
5. Random Forest threshold selection using validation data.
6. Final evaluation on the held-out test set.

## Final Test Results

| Metric | Score |
|---|---:|
| Fraud precision | 0.9286 |
| Fraud recall | 0.7324 |
| Fraud F1-score | 0.8189 |
| PR-AUC (Average Precision) | 0.8111 |
| Selected threshold | 0.3200 |

## Key Findings

- Fraud detection is an imbalanced classification problem.
- Threshold selection changes the balance between recall and false alarms.
- The final model's threshold was selected on validation data, then
  evaluated on the separate test set.
- The model is a portfolio demonstration, not a production banking system.

## Project Files

- `- `fraud_detection.ipynb`: main analysis notebook
- `business_insights.md`: business findings and limitations
- `final_metrics.json`: final test metrics
- `classification_report.csv`: classification metrics
- `confusion_matrix.png`: final test confusion matrix
- `threshold_optimization.png`: validation threshold analysis

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.

## Reproducibility

Use Google Colab or a compatible Python environment. Download the dataset
from the source linked above and update the input path as needed.
