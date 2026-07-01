# Problem Definition

## 1. Problem Statement

This project aims to develop an end-to-end data-driven customer churn prediction platform that enables the bank to identify customers who are at risk of leaving before they churn.

Rather than predicting only whether a customer will churn, the system will estimate each customer's **probability of churn**, classify customers as **Churn** or **Non-Churn**, and generate a **ranked list of high-risk customers**. This allows Relationship Managers and Marketing Teams to prioritize customers for retention campaigns based on their level of risk.

Beyond prediction, the project also establishes a complete analytics and machine learning workflow, including data engineering, business analytics, feature engineering, model development, explainability, and production deployment to support reliable and scalable decision-making.

---

## 2. Problem Type

* **Business Problem:** Customer Retention
* **Data Science Problem:** Customer Churn Prediction
* **Machine Learning Type:** Supervised Learning
* **Learning Task:** Binary Classification

---

## 3. Prediction Target

* **Target Variable (y):** Churn
* **Class Labels:**

  * **0:** Non-Churn (Customer is expected to remain)
  * **1:** Churn (Customer is expected to leave)

---

## 4. Prediction Unit

Each record in the dataset represents a single customer, and the model generates predictions independently for every customer.

---

## 5. Input Features

The model will use customer information available before prediction, including but not limited to:

* Customer demographics
* Account information
* Banking relationship
* Product ownership and usage
* Financial behavior
* Customer activity
* Historical interactions

The final feature set will be determined through data exploration, business analysis, and feature engineering.

---

## 6. Model Output

For each customer, the system will generate:

* Churn probability (risk score)
* Predicted class (Churn / Non-Churn)
* Customer risk ranking
* Priority list for retention campaigns
* Explanation for prediction (key factors and top contributing drivers behind the churn risk score)

These outputs will support Relationship Managers in identifying and prioritizing customers who should be contacted first.

---

## 7. Prediction Frequency

Predictions will be generated daily through a batch prediction pipeline. The generated customer risk list will support daily retention planning and customer engagement activities.

---

## 8. Decision Threshold

The classification threshold will initially use a default value and may be optimized during model evaluation to achieve an appropriate balance between business objectives and machine learning performance.

---

## 9. Assumptions

* Historical labeled customer data is available.
* Customer records are uniquely identifiable.
* Required input features are available before prediction.
* Customer information is updated regularly.
* Historical churn labels accurately represent customer behavior.

---

## 10. Edge Cases

The solution should account for situations such as:

* Missing feature values
* Duplicate customer records
* New customers with limited historical history
* Invalid or unexpected input values
* Changes in customer behavior over time (data drift)

---

## 11. Out of Scope

The initial version of this project will not include:

* Real-time prediction
* Automated customer communication
* Automated campaign execution
* Online model retraining
* Multi-class churn prediction
* Customer lifetime value prediction
* Offer or incentive recommendation
