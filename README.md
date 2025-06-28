# Credit Card Fraud Detection

This repository contains a machine learning project aimed at identifying fraudulent credit card transactions.

## Author Details

* **Author**: Tushar Surja
* **Batch**: June 2025 batch B33
* **Domain**: Data Science

## Project Aim

The primary goal of this project is to build a robust machine learning model capable of accurately identifying fraudulent credit card transactions.

## Project Overview

This project addresses the critical problem of credit card fraud detection using a machine learning approach. It involves data loading, comprehensive preprocessing, handling class imbalance, model training, and evaluation to achieve high detection rates for fraudulent activities.

## Key Steps and Methodology

The following steps were performed in this project:

1.  **Data Loading**: The transaction data was loaded from a specified CSV file into a pandas DataFrame.
2.  **Data Preprocessing**:
    * Missing values were identified and handled by dropping corresponding rows.
    * Features (excluding 'Class' and 'Time') and the target variable ('Class') were separated.
    * Features were scaled using `StandardScaler` for optimal model performance.
    * The 'Time' column was dropped as it was deemed not directly relevant for fraud detection based on transactional features.
3.  **Handling Class Imbalance**: The significant class imbalance between fraudulent and non-fraudulent transactions was addressed using **SMOTE (Synthetic Minority Over-sampling Technique)** oversampling. This resulted in a balanced dataset with an equal number of instances for both classes (233,319 instances for each class).
4.  **Data Splitting**: The balanced dataset was split into training (80%) and testing (20%) sets using stratified sampling to ensure the class distribution was maintained in both subsets.
5.  **Model Training**: A Logistic Regression model was trained on the prepared and balanced training data.
6.  **Model Evaluation**: The trained model's performance was evaluated on the test set.

## Model Performance

The Logistic Regression model achieved the following performance metrics on the test set:

* **Precision**: Approximately 0.976
* **Recall**: Approximately 0.925
* **F1-score**: Approximately 0.950

## Insights and Next Steps

* The high precision indicates that when the model predicts a transaction as fraudulent, it is highly likely to be correct. This is crucial for minimizing false alarms and reducing unnecessary investigations.
* While the recall is also high, further exploration of other machine learning models or advanced techniques could potentially enhance the detection rate of actual fraudulent transactions, leading to an even more robust fraud detection system.

## Technologies and Libraries Used

* Python
* pandas
* scikit-learn (`StandardScaler`, `LogisticRegression`)
* imbalanced-learn (`SMOTE`)
