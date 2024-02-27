# Snowflake_MLOps

# Titanic Survival Prediction with Snowflake ML

This project showcases an end-to-end machine learning workflow using Snowflake's Snowpark Python API, focusing on predicting survival rates from the Titanic dataset. It demonstrates how to leverage Snowflake for data preprocessing, feature engineering, model training and evaluation, hyperparameter tuning, and model deployment.

## Overview

The goal of this project is to accurately predict the survival of passengers on the Titanic using various features such as class, sex, fare, and more. The workflow includes data cleaning, preparation, model training with hyperparameter tuning using grid search, and deploying the best model for predictions.

## Workflow Steps

1. Data Preparation: Load the Titanic dataset from Snowflake, identify and remove columns with null values or those that are unnecessary for the    prediction task, and cast certain columns to appropriate data types for modeling.

2. Feature Engineering:
    - Identify categorical and numerical columns.
    - Impute missing values in categorical columns using the most frequent value.
    - Apply one-hot encoding to categorical variables to prepare them for model input.

3. Model Training and Selection:
    - Split the dataset into training and testing sets.
    - Define a parameter grid and use `GridSearchCV` for hyperparameter tuning on an XGBoost classifier, optimizing for accuracy.
    - Evaluate the best model's performance on a test set.

4. Model Deployment:
    - Use Snowflake's model registry for versioning and logging the optimal model along with its evaluation metrics.
    - Deploy the best-performing model version for making predictions on new data.

## Key Features

- Snowflake for ML: Utilizes Snowflake's capabilities for data manipulation, machine learning model training, and deployment.
- Feature Engineering: Demonstrates how to prepare data for modeling within Snowflake using imputation and encoding techniques.
- Hyperparameter Tuning: Employs grid search to find the best hyperparameters for the XGBoost model, aiming to improve prediction accuracy.
- Model Registry and Deployment: Showcases how to log, version, and deploy models within Snowflake, facilitating easy access and management of     machine learning models.

## Technologies Used

- Snowflake Snowpark Python API
- XGBoost for classification
- Pandas for data manipulation and analysis
- Grid search for hyperparameter tuning

## Conclusion

This project exemplifies a complete machine learning pipeline within Snowflake, from data processing to model deployment, emphasizing the platform's strength in supporting data science and machine learning workflows. By utilizing Snowflake, we streamline the process of developing, tuning, and deploying machine learning models, enabling efficient prediction capabilities directly within the data warehouse environment.
