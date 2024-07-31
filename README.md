# Loan Default Prediction

## Overview

The dataset provided for this project is a subset of data our team worked on for a project of Bajaj Finserv. In the financial industry, it is crucial for lenders to assess the creditworthiness of borrowers before granting loans or credit. Identifying potential defaulters, who are at higher risk of failing to repay their debts, can help mitigate financial losses and maintain a healthy lending portfolio. The goal of this project is to develop a predictive model that can accurately classify borrowers as defaulters or non-defaulters based on various financial and demographic factors.

## Objectives

1. Create the best machine learning model (testing for accuracy) to predict defaulters and non-defaulters by analyzing historical data.
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
3. **Gradient Boosting and AdaBoost**
4. **Support Vector Machine (SVM)**
5. **Neural Networks**

We used SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance in the training data.

## Results

The results of each model were evaluated based on classification reports and accuracy scores. The model performances are summarized below:

- **Logistic Regression**: 
  - Without SMOTE: Accuracy: 79.8% and With SMOTE: Accuracy: 54.8% 
  - Important Features: loan_type, interest_rate, employment_type, income_level, gender, marital_status, and education_level
    
- **Random Forest**:
  - Without SMOTE: Accuracy: 79.7% and With SMOTE: Accuracy: 68.4% 
  - Important Features: interest_rate, loan_amount, credit_score, loan_term

- **Gradient Boosting Classifier and AdaBoost Classifier with SMOTE**:
  - Gradient Boosting: Accuracy: 58.8% and AdaBoost: Accuracy: 55.2% 

- **Support Vector Machine (SVM)**:
  - Without SMOTE: Accuracy: 79.8% and With SMOTE: Accuracy: 53.3% 
  - Important Features: education_level, loan_type, income_type, interest_rate

- **Neural Networks**:
  - Without SMOTE: Accuracy: 79.8% and With SMOTE: Accuracy: 54.8% 

Based on the evaluations, Random Forest Classifier with SMOTE was determined to be the best-performing model.

## Recommendations

- **Feature Importance**: The feature `interest_rate` was consistently important across different models for predicting the target variable, suggesting higher interest rates are associated with higher default probability.
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
    jupyter notebook notebooks/Predicting loan defaulters.ipynb
    ```

4. Evaluate the saved models using the provided test dataset.

## License

This project is licensed under the MIT License.

