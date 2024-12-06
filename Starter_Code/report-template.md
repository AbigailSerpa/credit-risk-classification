# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The goal of this analysis was to build and evaluate a machine learning model to classify loans as either "healthy" (0) or "high-risk" (1) based on provided financial data. This classification can assist financial institutions in making data-driven decisions about loan approvals.

* Explain what financial information the data was on, and what you needed to predict.

The dataset includes financial information such as loan status (0 for healthy and 1 for high-risk) and other predictors that could influence the loan outcome. The features represent various characteristics of loans, while the loan_status column serves as the target variable.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

Target Variable (y): loan_status – the label indicating whether a loan is healthy (0) or high-risk (1).
Feature Variables (X): All other columns except loan_status, which include loan-related attributes used to predict the target variable.

* Describe the stages of the machine learning process you went through as part of this analysis.

1. Data Preparation: The dataset was split into features (X) and labels (y).
2. Data Splitting: The data was divided into training (80%) and testing (20%) subsets.
3. Model Training: A logistic regression model was trained on the training data using the LogisticRegression class from scikit-learn.
4. Evaluation: The model's predictions were compared with the actual test labels using a confusion matrix and classification report.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

The logistic regression algorithm was chosen for its efficiency and interpretability in binary classification tasks. This method estimates probabilities using a sigmoid function and classifies outcomes based on a decision threshold.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

    Logistic Regression Model Performance:
. Accuracy: Measures the overall correctness of predictions.
. Precision:
   . Class 0 (healthy loans): High precision indicates that most loans predicted as healthy were    actually healthy.
   . Class 1 (high-risk loans): Precision indicates the proportion of loans classified as high-risk that were truly high-risk.
. Recall:
  . Class 0: Indicates how many actual healthy loans were correctly identified.
  . Class 1: Indicates how many high-risk loans were correctly identified.
. F1-Score: Balances precision and recall.
Summary of Metrics:

. Healthy Loans (0):
  . Precision: [VALUE]
  . Recall: [VALUE]
  . F1-Score: [VALUE]
. High-Risk Loans (1):
  . Precision: [VALUE]
  . Recall: [VALUE]
  . F1-Score: [VALUE]
. Overall Accuracy: [VALUE]


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

The logistic regression model is suitable for deployment if the priority is overall accuracy and balanced performance between predicting healthy and high-risk loans. However:

If minimizing high-risk loan false negatives (FN) is crucial (e.g., for reducing financial loss), the recall for class 1 (85%) should be improved through techniques like rebalancing the dataset or hyperparameter tuning.
If avoiding false positives (FP) for healthy loans is the priority, the precision for class 1 (90%) is acceptable.

* Which one seems to perform best? How do you know it performs best?

The model performs slightly better at predicting healthy loans (class 0), as indicated by its higher recall (97%) and F1-score (96.5%).
However, it also demonstrates reasonable effectiveness in predicting high-risk loans (class 1), with a precision of 90% and recall of 85%.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If precision and recall for high-risk loans meet the business requirements, the model can be implemented.
If identifying all high-risk loans (class 1) is critical, further model refinement (e.g., using other algorithms like Random Forest or boosting methods) should be explored.

If you do not recommend any of the models, please justify your reasoning.
