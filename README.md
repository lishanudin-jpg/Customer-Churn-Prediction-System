# Customer Churn Prediction System

## Project Overview

The Customer Churn Prediction System is a machine learning project that predicts whether a customer is likely to discontinue a service.

The system analyzes customer behavior and historical business information to identify customers who have a high probability of leaving. This can help businesses take proactive customer-retention actions.

## Objectives

- Perform customer data preprocessing.
- Handle missing values.
- Analyze customer churn patterns.
- Apply classification algorithms.
- Compare multiple machine learning models.
- Identify important features influencing churn.
- Predict individual customer churn probability.
- Classify customers into Low, Medium, and High risk.
- Evaluate model performance.
- Save the trained machine learning model.

## Dataset

The project uses a synthetic customer dataset containing 1,200 customer records.

### Target Variable

`Churn`

- `0` = Customer stays
- `1` = Customer churns

### Features

- CustomerID - Unique customer identifier
- TenureMonths - Number of months the customer has used the service
- MonthlyCharges - Customer's monthly service charge
- TotalCharges - Total amount charged to the customer
- Contract - Customer contract type
- InternetService - Type of internet service
- PaymentMethod - Customer payment method
- SupportTickets - Number of support tickets
- TechSupportCalls - Number of technical support calls
- SeniorCitizen - Whether the customer is a senior citizen
- Dependents - Whether the customer has dependents
- PaperlessBilling - Whether paperless billing is enabled
- Churn - Target variable

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

Note: Seaborn is not required for this project.

## Machine Learning Algorithms

The project compares four classification algorithms:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting

The final model used in the project is Random Forest.

## Project Workflow

Customer Dataset
        |
        v
Data Loading
        |
        v
Data Exploration
        |
        v
Missing Value Handling
        |
        v
Feature Preprocessing
        |
        v
Categorical Encoding
        |
        v
Numerical Feature Scaling
        |
        v
Train/Test Split
        |
        v
Classification Models
        |
        v
Model Comparison
        |
        v
Random Forest Selection
        |
        v
Model Evaluation
        |
        v
Feature Importance
        |
        v
Customer Risk Prediction
        |
        v
Save Trained Model

## Data Preprocessing

The following preprocessing techniques are applied:

- Customer ID is removed from the machine learning features.
- Missing numerical values are replaced using median imputation.
- Missing categorical values are replaced using the most frequent value.
- Categorical variables are converted using One-Hot Encoding.
- Numerical features are standardized using StandardScaler.
- The dataset is divided into training and testing data.

### Train/Test Split

Training Data: 80%

Testing Data: 20%

A stratified split is used to maintain the distribution of churn classes.

## Model Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### Accuracy

Accuracy measures the percentage of correctly classified customers.

### Precision

Precision measures how many customers predicted as churners actually churn.

### Recall

Recall measures how many actual churners are correctly identified.

### F1 Score

F1 Score provides a balance between precision and recall.

### ROC-AUC

ROC-AUC measures the model's ability to distinguish between customers who churn and customers who stay.

For a customer-retention system, Recall is particularly important because failing to identify a customer who is likely to churn can result in a lost customer.

## Customer Risk Prediction

The system calculates the probability that a customer will churn.

Customers are categorized into three risk levels:

- Below 30% - Low Risk
- 30% to below 70% - Medium Risk
- 70% or above - High Risk

Example:

Customer ID: CUST10245

Churn Probability: 82.50%

Prediction: LIKELY TO CHURN

Risk Level: HIGH

## Feature Importance

The Random Forest model is also used to identify features that have a strong influence on the prediction.

Feature importance helps businesses understand which customer characteristics are associated with churn predictions.

The notebook displays the top important features using a Matplotlib visualization.

## Project Structure

customer_churn_prediction/
|
|-- customer_churn.csv
|
|-- customer_churn_prediction.ipynb
|
|-- customer_churn_prediction.py
|
|-- churn_model.pkl
|
|-- performance_report.md
|
|-- README.md
|
|-- requirements.txt

## File Description

### customer_churn.csv

Contains the customer dataset used for training and testing the machine learning models.

### customer_churn_prediction.ipynb

The main Jupyter Notebook containing the complete machine learning workflow.

### customer_churn_prediction.py

Python source code containing the same core machine learning workflow.

### churn_model.pkl

The trained Random Forest machine learning model saved using Joblib.

### performance_report.md

Contains the model performance analysis, evaluation results, limitations, and future improvements.

### README.md

Project documentation and setup instructions.

### requirements.txt

Contains the Python libraries required to execute the project.

## Installation

Open a Jupyter Notebook cell and run:

%pip install pandas numpy matplotlib scikit-learn joblib

No Seaborn installation is required.

## How to Run the Project

### Step 1 - Download the Project

Download or clone the project repository.

### Step 2 - Open Jupyter Notebook

Start Jupyter Notebook:

jupyter notebook

### Step 3 - Open the Notebook

Open:

customer_churn_prediction.ipynb

### Step 4 - Make Sure the Dataset Is Available

Keep:

customer_churn.csv

in the same folder as the notebook.

### Step 5 - Run the Notebook

Run the cells from top to bottom.

The notebook will perform:

- Load Dataset
- Preprocess Data
- Train Models
- Compare Models
- Evaluate Random Forest
- Display Confusion Matrix
- Display ROC Curve
- Analyze Feature Importance
- Predict Customer Risk
- Save Model

## Model Output

The project generates:

- Dataset analysis
- Missing-value analysis
- Churn distribution
- Model comparison table
- Classification report
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- ROC Curve
- Feature importance
- Customer churn probability
- Customer risk classification
- Trained model file

## Business Application

Businesses can use a churn prediction system to identify customers who may be at risk of leaving.

For example, high-risk customers could be considered for:

- Customer-support follow-ups
- Service-quality reviews
- Personalized offers
- Contract renewal communication
- Loyalty programs
- Customer satisfaction surveys

The model should be used as a decision-support tool rather than as the sole basis for business decisions.

## Limitations

- The included dataset is synthetic and intended for educational and portfolio purposes.
- Results may differ when the model is trained on real-world customer data.
- Customer behavior can change over time.
- Model predictions are probabilities and are not guaranteed outcomes.
- Real-world deployment would require continuous monitoring and retraining.

## Future Enhancements

The project can be improved by adding:

- Streamlit interactive web interface
- Real-world customer churn dataset
- Hyperparameter tuning
- Cross-validation
- SHAP model explainability
- Automated model retraining
- Customer-retention recommendation system
- Database integration
- Cloud deployment using AWS
- Model monitoring
- API-based prediction service

## Conclusion

The Customer Churn Prediction System demonstrates an end-to-end machine learning workflow for predicting customer churn.

The project covers:

Data Preprocessing
+
Exploratory Data Analysis
+
Classification
+
Feature Analysis
+
Model Evaluation
+
Customer Risk Prediction
+
Model Deployment Preparation

This project provides a practical foundation for developing an intelligent customer-retention system using machine learning.
