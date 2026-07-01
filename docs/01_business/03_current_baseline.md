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