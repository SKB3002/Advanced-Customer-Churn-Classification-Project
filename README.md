# Advanced-Customer-Churn-Classification-Project

1. Project Objective
This project aims to predict customer churn for a telecom company using customer demographic and service usage data. By identifying customers at high risk of churn, the company can proactively implement targeted retention strategies to reduce financial loss and improve customer satisfaction.

2. Dataset Summary
The dataset includes information on 7,043 customers, capturing both demographic details (gender, senior citizen status, etc.) and usage patterns (internet service, online security, contract type, etc.). The churn rate in the dataset is approximately 26.5%, indicating a significant opportunity for customer retention.

3. Key Insights from Exploratory Data Analysis (EDA)
Customers with month-to-month contracts have a much higher churn rate than those with long-term contracts.

Lack of online security or tech support is associated with higher churn.

Higher monthly charges are strongly linked to churn.

MonthlyCharges and TotalCharges are positively correlated (ρ = 0.65).

Customers without partners or dependents are more likely to churn.

4. Modeling Approach
Multiple models were tested including Logistic Regression, Random Forest, and XGBoost. Feature engineering involved the creation of variables like IsFamily, encoding categorical features, and handling missing values appropriately. Hyperparameter tuning was applied using GridSearchCV.

5. Final Results (Tuned XGBoost)
| Metric               | Score      |
| -------------------- | ---------- |
| Accuracy             | 73%        |
| Precision            | 49%        |
| Recall (Churn class) | 80%        |
| F1-score             | 0.61       |
| ROC AUC              | **0.84** ✅ |
The model is optimized for high recall to ensure most churn-prone customers are identified, even if it means slightly lower precision.

6. Business Impact
With an 84% ROC AUC score and high churn recall, this model can help:

Identify at-risk customers and trigger retention offers (discounts, loyalty rewards).

Prioritize outreach to customers with short-term contracts or lacking support services.

Bundle high-risk services (like online security) to reduce churn.

7. Strategic Recommendations
Offer incentives to convert month-to-month contracts to longer-term ones.

Launch proactive support for users without tech help or online security.

Use personalized offers based on churn risk score to retain valuable customers.

Integrate the model in CRM systems via API to flag churn risk in real-time.
