## Overview of the Analysis

### Purpose of the Analysis
The purpose of this analysis is to develop and evaluate machine learning models to assess the creditworthiness of borrowers. We aim to leverage historical lending data from a peer-to-peer lending services company to build predictive models that can identify loans at high risk of default.

### Financial Data
The dataset used in this analysis contains historical lending activity data, including information about borrowers and loan outcomes. Specifically, we focus on the "loan_status" column, where a value of 0 indicates a healthy loan, and a value of 1 indicates a high risk of default.

### Variables of Interest
In our analysis, we are primarily interested in predicting the credit risk of loans. The key variables include:
- **Features (x)**: Various attributes from the dataset, such as borrower information, loan details, and financial indicators.
- **Labels (y)**: The "loan_status" column, where 0 represents healthy loans, and 1 represents high-risk loans.

### Machine Learning Process
Our analysis involved the following stages:
1. Data Preprocessing: Reading and preparing the data, including splitting it into training and testing sets.
2. Model Building: Training logistic regression models using the training data.
3. Model Evaluation: Assessing model performance through metrics like accuracy, precision, and recall.
4. Reporting: Summarizing and communicating the results of our analysis.

### Methods Used
We employed logistic regression, a commonly used classification algorithm, to model the credit risk. Additionally, we used resampling techniques to address potential class imbalance issues in the dataset.

## Results

### Machine Learning Model 1: Logistic Regression with Original Data
#Accuracy: Model 1 achieved a high accuracy score of approximately 94.4%, indicating that it performs well in classifying both healthy (0) and high-risk (1) loans.

#Precision and Recall: The precision for high-risk loans (1) is 0.87, indicating that when the model predicts a loan as high-risk, it is correct 87% of the time. The recall for high-risk loans is 0.89, implying that the model correctly identifies 89% of all high-risk loans in the dataset. These values suggest that while the model is reasonably good at identifying high-risk loans, there is room for improvement.

#Confusion Matrix: The confusion matrix reveals that the model correctly predicted most of the healthy loans (true negatives: 18679) but had some false negatives (67). It also identified many true positives (558) for high-risk loans but had some false positives (80).

### Machine Learning Model 2: Logistic Regression with Resampled Training Data
#Accuracy: Model 2, trained with oversampled data, achieved a significantly higher accuracy score of approximately 99.6%. This suggests that the oversampling technique improved the model's overall performance.

#Precision and Recall: The precision for high-risk loans (1) remained at 0.87, indicating a consistent ability to correctly classify high-risk loans. However, the recall for high-risk loans increased to 1.00, indicating that the model now correctly identifies all high-risk loans in the dataset. This is a significant improvement from Model 1.

#Confusion Matrix: The confusion matrix for Model 2 shows that it correctly predicted almost all healthy loans (true negatives: 18668) and correctly identified all high-risk loans (true positives: 623). There were only a few false negatives (2) and false positives (91).

## Summary

Model Comparison: Model 2, which was trained with resampled data using the RandomOverSampler, outperforms Model 1 in terms of accuracy, recall, and overall predictive capability. It demonstrates the ability to correctly identify all high-risk loans while maintaining good precision for high-risk loans.

Problem Dependency: The choice of which model to use may depend on the specific problem we are trying to solve. If it is more important to accurately identify high-risk loans (1's), then Model 2 is the clear choice due to its higher recall. However, if a balance between precision and recall is crucial, further fine-tuning and evaluation might be necessary.

Recommendation: Considering the substantial improvement in performance, Model 2, trained with oversampled data, is recommended for assessing credit risk. It offers a higher level of confidence in identifying high-risk loans, which is a crucial task for a lending services company.

Justification: The justification for recommending Model 2 is based on its superior performance in terms of recall, which ensures that all high-risk loans are correctly identified. This is especially important for risk assessment in the lending industry, as missing a high-risk loan can lead to financial losses.

Overall, the analysis demonstrates that employing data resampling techniques can significantly enhance the predictive capabilities of machine learning models in scenarios with imbalanced datasets, such as credit risk assessment.
