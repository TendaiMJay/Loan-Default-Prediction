# Loan Default Prediction

## Overview

The dataset provided for this project is a subset of data our team worked on for a project of Bajaj Finserv. In the financial industry, it is crucial for lenders to assess the creditworthiness of borrowers before granting loans or credit. Identifying potential defaulters, who are at higher risk of failing to repay their debts, can help mitigate financial losses and maintain a healthy lending portfolio. The goal of this project is to develop a predictive model that can accurately classify borrowers as defaulters or non-defaulters based on various financial and demographic factors.

## Objectives

1. Create a machine learning model to predict defaulters and non-defaulters by analyzing historical data.
2. Provide recommendations on which features are important for predicting the target variable.

## Data

The dataset includes various features related to the borrowers' financial and demographic information. The primary columns in the dataset are:

- `customer_id`
- `loan_id`
- `loan_type`
- `loan_amount`
- `interest_rate`
- `loan_term`
- `employment_type`
- `income_level`
- `credit_score`
- `gender`
- `marital_status`
- `education_level`
- `application_date`
- `approval_date`
- `disbursement_date`
- `due_date`
- `default_status` (target variable)

## Data Preparation

1. **Handling Missing Values**: Imputed missing values using mean for numerical features and mode for categorical features.
2. **Encoding Categorical Variables**: Used Label Encoding for categorical features.
3. **Scaling Numerical Features**: Applied Standard Scaler to standardize numerical features.
4. **Creating Custom Features**: Derived additional features as required (example: loan-to-income ratio).

## Model Training and Evaluation

We trained and evaluated the following models:

1. **Logistic Regression**
2. **Random Forest**
3. **Support Vector Machine (SVM)**
4. **Neural Networks**

We used SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance in the training data.

## Results

The results of each model were evaluated based on classification reports and accuracy scores. The model performances are summarized below:

- **Logistic Regression**: 
  - Accuracy: X.XX
  - Important Features: interest_rate, credit_score, loan_amount

- **Random Forest**:
  - Accuracy: X.XX
  - Important Features: credit_score, loan_amount, interest_rate

- **Support Vector Machine (SVM)**:
  - Accuracy: X.XX
  - Important Features: credit_score, loan_amount, interest_rate

- **Neural Networks**:
  - Accuracy: X.XX
  - Important Features: credit_score, interest_rate, loan_amount

Based on the evaluations, [Model Name] was determined to be the best-performing model.

## Recommendations

- **Feature Importance**: The features `credit_score`, `loan_amount`, and `interest_rate` were consistently important across different models for predicting the target variable.
- **Further Improvements**: Additional data, such as detailed income information or other financial indicators, could further enhance the model's predictive power.

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Loan_Default_Prediction.git
    cd Loan_Default_Prediction
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook for data preparation and model training:
    ```bash
    jupyter notebook notebooks/data_preparation_and_modeling.ipynb
    ```

4. Evaluate the saved models using the provided test dataset.

## License

This project is licensed under the MIT License.

## Acknowledgements

This project was completed as part of a collaborative effort within our team at [Your Company]. Special thanks to Bajaj Finserv for providing the dataset.

