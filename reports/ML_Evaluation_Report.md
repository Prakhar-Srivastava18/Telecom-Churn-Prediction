# Machine Learning Model Evaluation Report

Project: Telecom Customer Churn Prediction

Prepared by: Prakhar Srivastava

# Model Performance Metrics

The dataset was split into an 80% training set and a 20% testing set. Features were standardized using a StandardScaler. The baseline model (Logistic Regression) was compared against an ensemble method (Random Forest).

**Model 1: Logistic Regression**

Testing Accuracy: 78.54%

Precision (Churn): 0.61

Recall (Churn): 0.52

F1-Score (Churn): 0.56


**Model 2: Random Forest**

Testing Accuracy: 79.03%

Precision (Churn): 0.63

Recall (Churn): 0.50

F1-Score (Churn): 0.56


🔍 Technical Performance Analysis

Why Random Forest Performed Better?

The Random Forest Classifier achieved the higher overall accuracy (79.03%).

Handling Non-Linear Relationships: Logistic Regression assumes a linear relationship between the features and the log-odds of churning. However, relationships in telecom data are highly non-linear (e.g., churn risks are high at very low tenures, stabilize, and then rise again if monthly charges spike). Random Forest uses decision trees to partition data non-linearly, catching these boundaries easily.

Feature Interactions: Random Forest naturally captures interactions between variables (e.g., a customer who has both a Month-to-Month contract and Fiber Optic internet is at extreme risk). Logistic Regression cannot capture these interactions without manual feature engineering.

Why Logistic Regression is Still Valuable?

Model Explainability: Logistic Regression is mathematically simpler. We can look directly at the model's coefficients to understand exactly how much a $1 increase in monthly charges increases the risk of churn.

Computational Efficiency: Logistic Regression trains in milliseconds, whereas Random Forest requires constructing hundreds of decision trees, which takes more system memory and processing power.

💡 Short Conclusion & Business Recommendations :-

Onboarding Strategy: Since the model flags new, high-paying customers on Month-to-Month contracts as high-risk, the business should offer automated loyalty discounts or free "Tech Support" during their first 90 days.

Autopay Incentives: Transition Electronic Check users to automatic Credit Card payments by offering a small monthly incentive (e.g., $2 off), as automated billing reduces churn triggers.