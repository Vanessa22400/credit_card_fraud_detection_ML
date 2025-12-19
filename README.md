# Credit Card Fraud Detection using Machine Learning

This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques applied to a highly imbalanced real-world dataset.

The goal is to build and evaluate models that can identify fraudulent behavior while minimizing false alerts, which is a key challenge in fraud detection systems.

---

## Business Problem

Financial institutions process millions of transactions every day, making manual fraud detection impractical. Automated systems are required to quickly flag suspicious transactions for further investigation.

From a business perspective, fraud detection involves balancing two critical outcomes:
- Missing fraudulent transactions, which can lead to financial loss
- Incorrectly blocking legitimate transactions, which harms customer experience

An effective fraud detection model should identify most fraudulent transactions while keeping false positives at an acceptable level.

---

## Dataset

The dataset used in this project comes from Kaggle and contains credit card transactions made by European cardholders in September 2013.

- **Total transactions:** 284,807  
- **Fraudulent transactions:** 492 (~0.17%)

For privacy reasons, all features were anonymized using Principal Component Analysis (PCA).

**Main variables:**
- `V1` to `V28`: PCA-transformed features  
- `Time`: Seconds elapsed since the first transaction  
- `Amount`: Transaction amount  
- `Class`: Target variable (1 = fraud, 0 = legitimate)

Due to the strong class imbalance, accuracy alone is not a reliable metric for this problem.

---

## Exploratory Data Analysis

During the exploration phase, the following aspects were analyzed:
- Class imbalance between fraudulent and legitimate transactions
- Distribution of transaction amounts
- Differences in feature behavior between fraud and non-fraud cases

Even with anonymized features, meaningful patterns were observed that help distinguish fraudulent behavior.

---

## Data Preparation

The data preparation process included:
- Splitting the dataset into training and test sets
- Scaling the `Amount` feature
- Handling class imbalance using class weighting during model training

Class imbalance was addressed at the model level, without modifying the original data distribution.

---

## Modeling

Two models were trained and evaluated:

### Logistic Regression (Baseline Model)
Logistic Regression was used as a baseline model due to its simplicity and interpretability. Class weights were applied to give more importance to fraudulent transactions.

- High recall for fraud detection
- Very low precision, resulting in many false positives
- Strong ROC-AUC score

This model is useful as a baseline but less suitable for real-world deployment on its own.

### Random Forest (Final Model)
Random Forest was selected as a more powerful model capable of capturing non-linear relationships and complex feature interactions.

- Much better balance between precision and recall
- Significant reduction in false positives
- Strong overall performance

---

## Model Comparison

Although both models achieved high ROC-AUC scores, their behavior differed substantially:

- **Logistic Regression** prioritized recall, detecting most fraud cases but generating many false alerts
- **Random Forest** achieved a more balanced performance, maintaining strong fraud detection while reducing false positives

Based on these results, **Random Forest was selected as the final model** for this project.

---

## Limitations

- PCA-transformed features limit interpretability and domain-specific analysis
- The dataset represents a specific region and time period
- No cost-sensitive evaluation was performed, despite different business impacts of errors

---

## Next Steps

Possible improvements include:
- Applying resampling techniques such as SMOTE or undersampling
- Testing additional models like Gradient Boosting and XGBoost
- Performing hyperparameter tuning
- Exploring precision-recall curves and threshold optimization
- Incorporating cost-sensitive evaluation

---

## Author

**Vanessa Donato**  
Data Scientist | Python | Machine Learning  
Impact-driven projects
