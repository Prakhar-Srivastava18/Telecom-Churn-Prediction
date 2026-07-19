# Telecom Customer Churn Prediction 📉

## Project Overview
This project analyzes a Telecom dataset to discover why customers leave (churn) and builds machine learning models to predict future churn. 

* **[View the full EDA Insights Report here](reports/EDA_Insights_Report.md)**
* **[View the full ML Evaluation Report here](reports/ML_Evaluation_Report.md)**

## Project Phases
1. **Data Cleaning:** Handled missing `TotalCharges` values and removed inconsistent formatting.
2. **Exploratory Data Analysis (EDA):** Discovered that customers with Month-to-Month contracts and high monthly charges are most likely to churn. Also found a strong correlation (0.83) between Tenure and Total Charges.
3. **Machine Learning:** Trained Logistic Regression and Random Forest models. 

## Key Visualizations

### The "Early-Exit" Trend
Customers are highly likely to cancel in their first few months. If they stay past a year, loyalty increases dramatically.
![Tenure Distribution](images/Customer%20Tenure%20Distribution%20by%20Churn.png)

### Price Sensitivity
Customers who churn tend to have significantly higher average monthly charges (~$80) compared to those who stay (~$65).
![Monthly Charges Boxplot](images/Monthly%20Charges%20vs%20Churn%20(Boxplot).png)

### Contract Risk
Customers on month-to-month contracts are vastly more likely to churn than those locked into 1-year or 2-year contracts.
![Contract Type](images/Churn%20by%20Contract%20Type.png)

## Results
* **Logistic Regression Accuracy:** 78.54%
* **Random Forest Accuracy:** 79.03%
* **Conclusion:** The Random Forest model slightly outperformed the baseline, likely due to its ability to capture complex, non-linear patterns in customer behavior.

## Technologies Used
*   Python
*   Pandas
*   Seaborn
*   Matplotlib
*   Scikit-Learn

## How to Run
1.  Clone this repository.
2.  Install the required dependencies using `pip install -r requirements.txt`.
3.  Navigate to the `notebooks/` folder and open the Jupyter Notebooks in the following order to reproduce the analysis:
    *   `cleaning_code.ipynb`
    *   `EDA.ipynb`
    *   `3_Machine_Learning.ipynb`