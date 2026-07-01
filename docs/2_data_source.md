# Data Source

## Dataset Name

**Bank Customer Churn Prediction Dataset**

---

## Source

This project uses the **Bank Customer Churn Prediction** dataset obtained from a publicly available machine learning repository (e.g., Kaggle). The dataset is intended for educational and research purposes and is widely used for binary classification problems involving customer churn prediction.

---

## Why This Dataset?

This dataset was selected because it:

* Represents a realistic customer churn problem in the banking industry.
* Contains historical customer information suitable for supervised machine learning.
* Includes a labeled target variable (`Churn`/`Exited`) required for binary classification.
* Provides sufficient customer demographic, account, and financial features for predictive modeling.
* Is widely used by the machine learning community, making it suitable for learning and benchmarking.

---

## Dataset Overview

* **Domain:** Banking
* **Problem Type:** Customer Churn Prediction
* **Machine Learning Task:** Binary Classification
* **Prediction Target:** Customer Churn (`0 = Non-Churn`, `1 = Churn`)
* **Prediction Unit:** One customer per record

---

## Intended Use

The dataset will be used to:

* Understand customer characteristics associated with churn.
* Build and evaluate a machine learning model that predicts customer churn.
* Demonstrate an end-to-end production-style machine learning workflow, including data validation, preprocessing, model development, evaluation, and deployment.

---

## Assumptions

The following assumptions are made for this project:

* Historical customer data is representative of future customer behavior.
* The target labels correctly indicate whether a customer churned.
* Each row represents a unique customer.
* The available features can be used at prediction time.

---

## Dataset Limitations

* The dataset represents a simplified banking scenario and may not capture all factors influencing customer churn.
* Customer behavior and market conditions may differ from those of real financial institutions.
* Some potentially useful business features (e.g., customer support interactions, marketing campaign history, transaction-level data) are not included.
* The dataset is static and does not reflect changes in customer behavior over time.

---

## Future Improvements

For a production system, additional data sources could improve model performance, such as:

* Transaction history
* Customer support interactions
* Digital banking activity
* Marketing campaign responses
* Customer feedback and satisfaction metrics
* Product usage history
