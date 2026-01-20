## data science project fraud detection

Fraud Detection System – End-to-End Machine Learning Project

**1.0 Business Problem**

Financial institutions face a major challenge in identifying fraudulent transactions in real time.
Manual monitoring is slow, error-prone, and not scalable.

Objective:
Build a machine learning model that can predict whether a transaction is fraudulent or legitimate based on transaction details, and deploy it as a simple web application.

**2.0 Business Assumptions**

Historical transaction data contains patterns that distinguish fraud from non-fraud.

Transaction attributes such as amount, balances, and transaction type are relevant predictors.

Fraud detection is treated as a binary classification problem.

The trained model will generalize reasonably well on unseen transaction data.

**3.0 Solution Strategy**

The solution was developed using an end-to-end data science workflow:

Performed Exploratory Data Analysis (EDA) in Jupyter Notebook

Cleaned and prepared data for modeling

Built a machine learning pipeline including preprocessing and model training

Trained a Logistic Regression model

Saved the trained pipeline using joblib

Deployed the model using a Streamlit web application

**4.0 Top 3 Data Insights**

Certain transaction types (e.g., TRANSFER and CASH_OUT) show higher association with fraudulent activity.

Fraudulent transactions often involve large transaction amounts compared to normal transactions.

Balance differences before and after transactions provide useful signals for fraud detection.![WhatsApp Image 2026-01-20 at 11 27 37 AM](https://github.com/user-attachments/assets/34e652a4-52cf-42d9-be8c-c091ceef5892)


**5.0 Machine Learning Applied**

Problem Type: Binary Classification

Model Used: Logistic Regression

Preprocessing:

Categorical encoding using OneHotEncoder

Numerical feature scaling using StandardScaler

Pipeline created using ColumnTransformer and Pipeline from Scikit-learn

Entire preprocessing + model combined into a single reusable pipeline

**6.0 Machine Learning Performance**

The machine learning model was evaluated on the test dataset using a trained pipeline.

Evaluation Metric Used: Accuracy

Model Accuracy: 94.59%

The accuracy score was calculated using:

pipeline.score(X_test, y_test)


This indicates that the model correctly classifies approximately 94.6% of the transactions in the test dataset.

The trained pipeline used for evaluation is the same pipeline saved using joblib and deployed in the Streamlit application, ensuring consistency between model evaluation and production usage.

Detailed evaluation such as classification report and confusion matrix were analyzed during experimentation and can be found in the Jupyter Notebook (01_EDA.ipynb).

**7.0 Business Results**

The model can automatically flag potentially fraudulent transactions.

Reduces dependency on manual review processes.

Provides a fast and scalable fraud screening mechanism.

Deployed Streamlit app enables easy, non-technical usage for business users.

**8.0 Conclusions**

A complete fraud detection system was successfully built and deployed.

Using a machine learning pipeline ensured clean and maintainable code.

Streamlit made model deployment simple and interactive.

The project demonstrates a real-world application of machine learning in finance.

**9.0 Lessons Learned**

Importance of proper EDA before modeling.

Benefits of using pipelines for preprocessing and training.

Clear separation of:

Notebook (analysis)

Scripts (deployment)

Models (artifacts)

Learned how to move from model building to real deployment.
