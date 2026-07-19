📊 Exploratory Data Analysis (EDA) Report

Project: Telecom Customer Churn Analysis

Prepared by: Prakhar Srivastava

Dataset: 7,043 Customers, 21 Features (Cleaned)

🔍 Outlier, Trend, & Pattern Identification

Before analyzing individual variables, we analyzed the dataset's mathematical distribution:

Outliers in Charges: By analyzing our boxplots and checking the Interquartile Range (IQR), we observed that while MonthlyCharges follow a stable bimodal distribution, TotalCharges is highly skewed to the right due to customer tenure variance. However, no data points were removed as outliers because high charges are logical for multi-year customers.

The "Early-Exit" Trend: A critical structural pattern was discovered in the first-quarter tenure groups, where customer churn behaves almost exponentially—extreme risk in month 1, which rapidly decays with every passing month.

Multicollinearity Pattern: A strong linear pattern exists between tenure and TotalCharges (correlation of 0.83). This makes mathematical sense: long-term loyal customers naturally accumulate higher total bills.

💡 10 Comprehensive Written Insights

1. The Critical "First-Month" Churn Hazard

The tenure distribution reveals a massive, alarming spike in churn during the first month of service (nearly 600 customers). If a customer survives their first 5 months, their probability of leaving drops by over 70%.

2. High Monthly Bills Drive Churn

The median monthly charge for customers who churned (approx. $80) is significantly higher than that of loyal customers (approx. $65). Customers are highly sensitive to premium price points.

3. Month-to-Month Contracts are High Risk

Customers on Month-to-Month contracts exhibit the absolute highest rate of churn. Conversely, those on One-Year and Two-Year contracts rarely leave, proving that contract lock-ins are the company's strongest retention tool.

4. Fiber Optic Internet is a Pain Point

Surprisingly, customers subscribed to Fiber Optic internet churn at a much higher rate than those on DSL, despite Fiber being faster. The business should immediately investigate the Fiber Optic tier for service outages or pricing misalignments to prevent losing premium customers.

5. Tech Support is a Strong Anchor

Customers who did not sign up for "Tech Support" or "Online Security" add-ons churned at a significantly higher rate. Providing free or discounted security/tech support bundles could dramatically increase retention.

6. Paperless Billing Correlates with Churn

Customers with Paperless Billing enabled show a higher tendency to churn. This may suggest that digital invoices make bill shocks (high monthly charges) more visible to customers, prompting them to cancel.

7. Senior Citizens are High-Risk

While Senior Citizens make up a smaller portion of the dataset, their churn rate is disproportionately high (approx. 42%) compared to younger demographics. The service or billing process may not be well-tailored for seniors.

8. Total Charges and Tenure Multicollinearity

The correlation matrix shows a very strong correlation of 0.83 between Tenure and Total Charges. If we feed both to a simple predictive model, it gets confused about which feature is actually driving the churn (a problem called multicollinearity). Therefore, we should drop one of these variables before training.

9. Electronic Check Payment Vulnerability

Customers paying via "Electronic Check" churn far more frequently than those using automated payment methods like Credit Cards or Bank Transfers. Friction in manual monthly payments increases the chance of cancellation.

10. Partner and Dependent Stability

Customers who have partners or dependents are significantly more stable and less likely to churn. Single individuals without dependents represent a highly volatile segment that requires targeted marketing.