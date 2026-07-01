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
