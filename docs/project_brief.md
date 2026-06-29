# Customer Churn Prediction Platform

## Project Brief

### Business Problem

The bank is losing valuable customers who contribute significantly to its revenue and long-term profitability. Currently, the bank lacks an effective way to identify customers who are likely to leave before they churn, limiting its ability to take timely retention actions.

### Why It Is a Problem

* Valuable customers often purchase multiple banking products and services.
* They generate recurring revenue and have a higher Customer Lifetime Value (CLV).
* Acquiring new customers is more expensive than retaining existing ones because it requires additional marketing and onboarding costs.
* Losing loyal customers negatively impacts long-term business growth and profitability.

### Business Opportunity

By identifying at-risk customers early and enabling timely retention strategies, the bank can:

* Increase customer retention.
* Reduce customer churn.
* Improve marketing campaign efficiency.
* Increase Customer Lifetime Value (CLV).
* Improve return on marketing investment.

---

## Current Baseline

### Current Manual Process
* The process is partially automated (CRM + rules) but heavily dependent on manual review.
* Relationship Managers and Marketing teams execute campaigns.
* CRM only helps to filter out data based on business rules. Static business rules cannot capture complex customer behavior.
* There is no intelligent system to prioritize customers based on their likelihood of churn.

### Rule-Based Heuristics

The bank currently uses predefined business rules to identify customers who may be at risk of churning. For example, customers with no transactions for a certain period, multiple complaints, or a significant drop in account balance may be flagged for review. While these rules are simple to implement and understand, they apply the same criteria to all customers and cannot capture complex patterns in customer behavior. As a result, they may incorrectly flag low-risk customers or fail to identify customers who are likely to churn despite not meeting the predefined rules.

### Competitor Product Analysis

Commercial platforms such as Salesforce Einstein provide AI-powered customer behavior prediction, CRM integration, and automated business insights. These platforms enable organizations to deploy predictive analytics quickly without developing custom machine learning models. However, they may involve high licensing costs, vendor lock-in, and limited flexibility for building highly customized ML pipelines. For this project, developing an in-house churn prediction system provides greater control over data, model customization, and integration with business-specific requirements.

### Cost of Not Solving the Problem

If the current approach is not improved, the bank may continue to lose valuable customers, leading to recurring revenue loss, higher customer acquisition costs, and inefficient marketing efforts. Relationship managers will continue spending significant time manually reviewing customer records, making it difficult to scale the process as the customer base grows. For demonstration purposes, assuming the bank has 100,000 customers with a 3% monthly churn rate, approximately 3,000 customers may leave each month. This illustrates the potential business impact of failing to identify at-risk customers early and take timely retention actions.

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


## Constraints & Requirements

The following constraints and requirements are assumed for this portfolio project to simulate a real-world production environment.

### Time Constraints

* Predictions will be generated **daily at 6:00 AM** as a batch process before the marketing team begins its workday.
* The system should complete prediction generation for all customers within **30 minutes**.
* Real-time prediction is not required for this project.

### Cost Constraints

* The project will be developed using **open-source technologies** and free development tools whenever possible.
* The target deployment environment assumes a **limited monthly infrastructure budget (approximately $50 USD/month)** suitable for a startup or proof-of-concept system.
* The solution should remain cost-effective while maintaining acceptable performance.

### Accuracy Requirements

* The model should achieve a **minimum ROC-AUC score of 0.85** on the test dataset.
* The model should maintain **high Recall (≥ 85%)** to identify as many potential churners as possible.
* Precision should be balanced to reduce unnecessary marketing campaigns while maintaining effective customer retention.

### Explainability Requirements

* Every prediction should be explainable to business stakeholders.
* The system should provide feature importance or explainability techniques (e.g., SHAP or feature importance) to help relationship managers understand why a customer was predicted to churn.
* Model transparency is preferred over using a completely black-box model.

### Data Constraints

* Historical customer data with churn labels is assumed to be available for model development.
* Customer data must be handled securely, and personally identifiable information (PII) should be excluded or anonymized where appropriate.
* The project assumes the use of an existing labeled dataset; therefore, no additional manual data labeling is required.

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


## Stakeholders & Their Needs

### 1. End Users

**Stakeholders:** Marketing Team and Relationship Managers

**Needs:**

* Receive a **daily prioritized list** of customers with the highest predicted churn risk.
* Access predictions through a **web dashboard or downloadable report**.
* View the predicted churn probability along with key reasons for each prediction to support retention decisions.
* Use predictions to prioritize customer outreach and retention campaigns.

### 2. Decision Makers

**Stakeholders:** Product Manager, Marketing Manager, and Bank Executives

**Needs:**

* Demonstrate measurable business value through improved customer retention and profitability.
* Justify the project's return on investment (ROI) and implementation costs.
* Understand project risks, expected timeline, and required resources before deployment.
* Monitor business KPIs such as customer retention, campaign efficiency, and profit improvement.

### 3. Maintainers

**Stakeholders:** Data Scientists, ML Engineers, and MLOps Engineers

**Needs:**

* Well-documented code, model, and data pipelines.
* Automated model retraining and deployment workflows.
* Monitoring dashboards for model performance and data quality.
* Logging, alerting, and deployment runbooks to ensure reliable system operation.

### 4. Data Providers

**Stakeholders:** Database Administrators, Data Engineering Team, and IT Department

**Needs:**

* Secure access to historical customer data.
* Compliance with data privacy and security policies.
* Reliable and regularly updated data pipelines.
* High-quality, complete, and consistent customer data for model training and prediction.

---



## Risk Assessment

The following risks have been identified for the proposed customer churn prediction system. The likelihood, impact, mitigation strategy, and monitoring approach are based on reasonable assumptions for this portfolio project.

| Risk Category | Risk                                                                    | Likelihood | Impact | Mitigation Strategy                                                                                    | Monitoring                                                                   |
| ------------- | ----------------------------------------------------------------------- | ---------- | ------ | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| **Data**      | Data quality issues (missing values, incorrect records, schema changes) | Medium     | High   | Implement automated data validation, schema checks, and preprocessing pipelines.                       | Monitor data quality reports and validation logs before each prediction run. |
| **Data**      | Customer behavior changes over time (data drift)                        | High       | High   | Periodically retrain the model using recent customer data.                                             | Monitor feature distributions and model performance metrics.                 |
| **Model**     | Model performance degrades after deployment                             | Medium     | High   | Schedule regular model evaluation and retraining.                                                      | Track Precision, Recall, ROC-AUC, and business KPIs over time.               |
| **Model**     | Biased or unfair predictions                                            | Low        | High   | Remove inappropriate features, evaluate fairness metrics, and perform bias analysis before deployment. | Periodically audit model predictions across customer groups.                 |
| **System**    | Daily prediction pipeline fails before business hours                   | Low        | High   | Implement automated retries, logging, and alerting mechanisms.                                         | Monitor pipeline execution status and receive failure notifications.         |
| **System**    | Unauthorized access to customer data                                    | Low        | Severe | Apply authentication, role-based access control, encryption, and secure credential management.         | Review access logs and perform regular security audits.                      |
| **Business**  | False predictions lead to inefficient marketing campaigns               | Medium     | Medium | Use probability thresholds, human review, and continuous model evaluation before campaign execution.   | Monitor campaign success rate, customer retention, and marketing ROI.        |
| **Business**  | Excessive reliance on model predictions                                 | Low        | Medium | Position the model as a decision-support tool rather than a fully automated decision-maker.            | Regularly review prediction outcomes with business stakeholders.             |
