## Success Definition

The success of this project will be evaluated based on measurable business outcomes. Since this is a portfolio project, the following targets are assumed for demonstration purposes.

### Business Success Metrics (Assumed Targets)

* **Increase Customer Retention Rate:** Improve the customer retention rate by **5%** through early identification of at-risk customers and targeted retention campaigns.
* **Reduce Marketing Costs:** Reduce retention campaign costs by **15%** by prioritizing customers with the highest predicted churn risk instead of contacting all customers.
* **Increase Business Profitability:** Increase annual profit from retained customers by **10%** through improved customer retention and higher customer lifetime value.

### Supporting Machine Learning Metrics

The business goals will be supported by monitoring machine learning performance metrics such as:

* Precision
* Recall
* F1-Score
* ROC-AUC

These metrics will be used to evaluate the predictive performance of the model and ensure it effectively supports the business objectives.

---

## Success Metrics Hierarchy

### Primary Business Metric

* **Customer Retention Rate:** The primary objective of this project is to increase customer retention by identifying at-risk customers early and enabling timely retention strategies.

### Secondary Machine Learning Metrics

* **Recall:** Prioritized to identify as many customers who are likely to churn as possible, minimizing missed retention opportunities.
* **Precision:** Used to reduce unnecessary retention campaigns by limiting false positive predictions.
* **ROC-AUC and F1-Score:** Monitored to evaluate the overall predictive performance and balance between Precision and Recall.

### Guardrail Metrics

* **Model Explainability:** Predictions should be interpretable so that business stakeholders understand why a customer is identified as high risk.
* **Fairness:** The model should avoid introducing bias against any customer group.
* **Prediction Latency:** Daily batch predictions should be completed before the marketing team begins its retention activities.