# Problem Definition

## 1. Machine Learning Problem Statement

This project aims to develop a supervised machine learning model that predicts whether a customer is likely to churn. The predictions will help the marketing and relationship management teams identify high-risk customers early and prioritize retention efforts, ultimately improving customer retention and business profitability.

---

## 2. Problem Type

* **Machine Learning Type:** Supervised Learning
* **Learning Task:** Binary Classification

---

## 3. Prediction Target

* **Target Variable (y):** Churn
* **Class Labels:**

  * **0:** Non-Churn (Customer stays)
  * **1:** Churn (Customer leaves)

---

## 4. Prediction Unit

Each record (row) in the dataset represents **one customer**, and the model predicts whether that customer is likely to churn.

---

## 5. Input Features

The model will use customer-related information available at prediction time, such as:

* Customer demographics
* Account information
* Product usage
* Transaction behavior
* Customer relationship history

The final list of features will be determined after data exploration.

---

## 6. Model Output

For each customer, the model will produce:

* A churn probability (0–1)
* A predicted class:

  * Churn
  * Non-Churn

These predictions will be used to prioritize customer retention activities.

---

## 7. Prediction Frequency

Predictions will be generated once every day at **6:00 AM** using a batch prediction pipeline. The marketing team will use the generated customer risk list to plan daily retention campaigns.

---

## 8. Decision Threshold

The default classification threshold is assumed to be **0.50** for this project. This threshold may be adjusted during model evaluation to achieve the desired balance between Precision and Recall based on business requirements.

---

## 9. Assumptions

* Historical labeled customer data is available.
* Customer records are uniquely identifiable.
* Input features are available before making predictions.
* Customer data is updated regularly.
* Churn labels accurately represent customer behavior.

---

## 10. Edge Cases

The system should consider the following situations:

* Missing feature values.
* Duplicate customer records.
* New customers with limited historical data.
* Unexpected feature values or invalid data.
* Data distribution changes over time (data drift).

---

## 11. Out of Scope

The first version of this project will not include:

* Real-time prediction.
* Automatic customer communication.
* Automatic marketing campaign execution.
* Continuous online model training.
* Multi-class churn prediction.
