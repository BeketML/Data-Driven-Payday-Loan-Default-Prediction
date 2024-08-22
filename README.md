# Credit Loan Default Prediction

This repository contains the code and documentation for predicting credit loan default using a dataset provided by a credit bureau. The main objective is to build a model that can accurately predict whether a client will default on a short-term loan.

## Dataset

The dataset includes data from 2023, with information on 73,420 clients. It is used to predict whether a client will default on a loan, which is denoted by the `default_status` attribute. This is a binary classification task where the model needs to predict one of two possible outcomes: default or no default.

### Columns

Here are the columns present in the dataset along with their descriptions:

- **`client_id`**: Unique identifier for each client.
- **`gender`**: Gender of the client (e.g., Male, Female).
- **`age`**: Age of the client.
- **`education_level`**: Client's level of education (e.g., High School, Bachelor's).
- **`owns_car`**: Indicates whether the client owns a car (1 for Yes, 0 for No).
- **`car_category`**: Category of the car owned by the client (e.g., economy, luxury, etc.).
- **`housing_status`**: Category of housing status (e.g., rent, own, etc.).
- **`job_prestige`**: Prestige category of the client's job.
- **`stable_employment`**: Indicates whether the client has stable employment (1 for Yes, 0 for No).
- **`annual_income`**: Client's annual income.
- **`travel_history`**: Indicates whether the client has a foreign passport and travel history.
- **`declined_applications`**: Number of previously declined loan applications.
- **`credit_score`**: Client's credit score based on bureau data.
- **`credit_inquiries`**: Number of credit inquiries made by credit bureaus.
- **`branch_category`**: Category of the branch based on channel and location.
- **`social_networking`**: Client's connections with other bank clients.
- **`info_update_recency`**: Recency of information update by the client.
- **`application_date`**: Date when the loan application was submitted (in datetime format with Eastern Time Zone).
- **`default_status`**: Indicates whether the client has defaulted on a loan (1 for Default, 0 for No Default).

## Model Evaluation Metrics

### Precision
Precision is the ratio of correctly predicted positive observations to the total predicted positives. It is a measure of the accuracy of the positive predictions.

### Recall
Recall (or Sensitivity) measures the proportion of actual positives that were correctly identified by the model. It reflects the model's ability to identify all relevant instances of the positive class.

### F1 Score
The F1 Score is the harmonic mean of Precision and Recall. It provides a single metric that balances both precision and recall, especially useful when the class distribution is imbalanced.

### ROC AUC Score
The ROC AUC Score represents the area under the Receiver Operating Characteristic curve. It evaluates the model's ability to distinguish between positive and negative classes. A higher AUC value indicates better model performance.

## Example Results

Here are the evaluation metrics for the model:

- **Precision**:
  - 0: 0.97
  - 1: 0.35

- **Recall**:
  - 0: 0.77
  - 1: 0.86

- **F1 Score**:
  - 0: 0.86
  - 1: 0.50

- **Accuracy**: 0.78

- **Macro Average**:
  - Precision: 0.66
  - Recall: 0.82
  - F1 Score: 0.68

- **Weighted Average**:
  - Precision: 0.90
  - Recall: 0.78
  - F1 Score: 0.82

- **ROC AUC Score**: 0.9006

## Model Optimization

To improve model performance, hyperparameter tuning was performed using Optuna. For LightGBM, the best hyperparameters were found to optimize model performance. The results and code for hyperparameter tuning are available in the repository.

## Dataset: https://www.kaggle.com/datasets/sokolovaleks/equifax-pdl-scoring-us-2023-csv
