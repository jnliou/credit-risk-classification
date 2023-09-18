# Credit Risk Classification

![Credit Risk Title](Credit_Risk/Resources/stock_risk.jpg)

## Overview

This project aims to assess the creditworthiness of borrowers using machine learning techniques. We leverage a dataset containing historical lending activity from a peer-to-peer lending services company to build predictive models capable of identifying loans at high risk of default.

## Repository Structure

The project repository is organized as follows:

- `Credit_Risk` Folder: Contains the Jupyter Notebook (`credit_risk_classification.ipynb`) where the data analysis, model development, and evaluation are performed, and (`credit_risk_analysis.md`) where the analysis report was recorded.
- `Resources` Folder: Contains the dataset file (`lending_data.csv`) used for analysis.
- `README.md` (This file): Provides an overview of the project, instructions, and analysis findings.

## Data

### Financial Data
The dataset includes various financial attributes, including:
- Loan size
- Interest rate
- Borrower income
- Debt-to-income ratio
- Number of accounts
- Derogatory marks
- Total debt
- Loan status (0 for healthy loans, 1 for high-risk loans)

## Analysis Steps

### 1. Data Preparation
- Read the dataset into a Pandas DataFrame.
- Separate labels (y) and features (X).
- Check the balance of the target variable (loan_status).
- Split the data into training and testing sets.

### 2. Model Development and Evaluation
#### Model 1: Logistic Regression with Original Data
- Fit a logistic regression model using the original training data.
- Evaluate the model's performance using metrics such as accuracy, precision, recall, and the confusion matrix.

#### Model 2: Logistic Regression with Resampled Training Data
- Utilize the RandomOverSampler to address class imbalance.
- Fit a logistic regression model using the resampled training data.
- Evaluate the resampled model's performance using the same metrics.

### 3. Analysis and Recommendation
- Compare the results of both models in terms of accuracy, precision, recall, and other relevant metrics.
- Provide recommendations based on the analysis findings regarding the choice of the best model for credit risk assessment.

## Results

### Model 1 (Logistic Regression with Original Data)
- Balanced Accuracy: Approximately 94.4%
- Precision for High-Risk Loans (1): 0.87
- Recall for High-Risk Loans (1): 0.89

### Model 2 (Logistic Regression with Resampled Training Data)
- Balanced Accuracy: Approximately 99.6%
- Precision for High-Risk Loans (1): 0.87
- Recall for High-Risk Loans (1): 1.00

## Summary and Recommendations

Based on the analysis results, Model 2, trained with resampled data using RandomOverSampler, is recommended for assessing credit risk. This model outperforms Model 1 in terms of accuracy, recall, and overall predictive capability. It demonstrates the ability to correctly identify all high-risk loans, which is crucial in the lending industry.

The choice of the recommended model may depend on the specific problem being addressed. If the primary goal is to accurately identify high-risk loans, Model 2 is the preferred choice due to its higher recall. However, for scenarios where a balance between precision and recall is critical, further fine-tuning and evaluation may be necessary.

## Dependencies

The analysis and modeling were performed using the following Python libraries:
- Pandas
- NumPy
- Scikit-Learn
- Imbalanced-Learn

## Usage

To replicate the analysis and results, follow these steps:
1. Clone this repository to your local machine.
2. Install the required Python libraries mentioned in the Dependencies section.
3. Open and run the Jupyter Notebook `credit_risk_classification.ipynb` in the `Credit_Risk` folder.

## Credits

This project was completed as part of a data analysis and machine learning challenge for the University of Toronto.

