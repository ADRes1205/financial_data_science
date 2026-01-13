# Credit Card Fraud Detection - Comparative Model Analysis

## Project Overview
Built and compared three machine learning classifiers (K-Nearest Neighbors, Logistic Regression, and Gaussian Naive Bayes) to detect fraudulent credit card transactions using anonymized transaction features.

## Business Case
Credit card fraud costs financial institutions billions annually. This project demonstrates:
- Automated fraud detection to reduce manual review workload
- Real-time transaction classification for immediate fraud prevention
- Model comparison to identify the most effective approach for imbalanced datasets
- Threshold optimization to balance fraud detection vs. false positives

## Technical Approach

**Models Tested:**
- K-Nearest Neighbors (k=5)
- Logistic Regression
- Gaussian Naive Bayes

**Key Techniques:**
- Handled highly imbalanced dataset (fraudulent transactions are rare)
- Compared models using multiple metrics: accuracy, precision, recall, Cohen's kappa
- Visualized decision boundaries to understand model behavior
- Generated ROC curves to evaluate model discrimination ability
- **Threshold tuning**: Adjusted classification threshold from 0.5 to 0.0002 to dramatically improve fraud detection rate

## Results

**Model Performance:**
- KNN: 99.86% accuracy, 83.57% precision, 23.78% recall
- Logistic Regression: 99.84% accuracy, 77.78% precision, 8.54% recall
- Gaussian Naive Bayes: 98.62% accuracy, 3.53% precision, 26.63% recall

**Threshold Optimization Impact:**
- Default threshold (0.5): Caught 26.6% of fraud cases
- Optimized threshold (0.0002): **Caught 82.1% of fraud cases**
- Trade-off: Increased false positive rate from 1.3% to 19.0%

## Business Impact
- **Fraud Detection Rate**: Increased from 26.6% to 82.1% through threshold optimization
- **Risk Management**: Demonstrated clear trade-off between catching fraud vs. customer friction from false alerts
- **Actionable Insights**: ROC analysis enables business to choose optimal threshold based on cost of fraud vs. cost of investigation

## Technologies Used
Python, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, MLxtend
