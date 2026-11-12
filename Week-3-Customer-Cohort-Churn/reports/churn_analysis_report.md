
# Customer Cohort & Churn Analytics Report

## 1. Project Overview

This project analyzes customer retention and churn behavior using the IBM Telco Customer Churn dataset.

The objective is to identify high-risk customer segments, analyze customer retention patterns, and provide strategic recommendations.

## 2. Dataset Information

- Dataset: IBM Telco Customer Churn
- Total Customers: 7,043
- Total Columns: 21
- Churned Customers: 1,869
- Retained Customers: 5,174

## 3. Baseline Churn Analysis

- Overall Churn Rate: 26.54%
- Overall Retention Rate: 73.46%

## 4. Customer Cohort Analysis

Customers were grouped based on subscription tenure:

- 0–12 Months
- 13–24 Months
- 25–36 Months
- 37–48 Months
- 49–60 Months
- 61–72 Months

The analysis shows that customer retention generally improves with increasing subscription tenure.

## 5. Contract Analysis

- Month-to-month churn: 42.71%
- One-year contract churn: 11.27%
- Two-year contract churn: 2.83%

Month-to-month customers have the highest observed churn rate.

## 6. Payment Method Analysis

Electronic check customers have the highest churn rate at 45.29%.

Automatic payment methods show comparatively lower churn rates.

## 7. High-Risk Customer Identification

Fiber Optic customers without technical support:

- Total Customers: 2,230
- Churned Customers: 1,101
- Churn Rate: 49.37%

This segment requires additional customer support and retention attention.

## 8. Monthly Charges Analysis

Customers in the high monthly charge category have a churn rate of 37.82%.

Personalized subscription plans and suitable pricing strategies may improve retention.

## 9. Strategic Recommendations

1. Improve onboarding for new customers.
2. Encourage long-term subscriptions.
3. Promote automatic payment methods.
4. Provide better technical support.
5. Introduce personalized pricing plans.
6. Monitor high-risk customer segments.

## 10. Conclusion

The analysis identified an overall churn rate of 26.54%.

Customer tenure, contract type, payment method, monthly charges, and technical support availability were examined to understand customer churn patterns.

The findings provide useful insights for improving customer retention and long-term business performance.

## 11. Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
