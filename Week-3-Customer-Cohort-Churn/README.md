# 📊 Week 3 – Customer Cohort & Churn Analytics

## 📌 Project Overview

This project focuses on analyzing customer retention behavior and identifying churn patterns using the **IBM Telco Customer Churn Dataset**.

The primary objective is to segment customers based on subscription tenure, contract types, payment methods, and monthly charges to identify high-risk customer segments and understand the factors associated with customer churn.

The analysis uses Python and data visualization techniques to generate actionable business insights and strategic customer retention recommendations.

## 🎯 Project Objectives

- Analyze customer churn and retention behavior.
- Calculate the overall customer churn rate.
- Segment customers into tenure-based cohorts.
- Analyze churn across different contract types.
- Investigate customer payment methods and monthly charges.
- Identify high-risk customer segments.
- Analyze Fiber Optic customers without technical support.
- Create cohort retention visualizations and churn heatmaps.
- Provide strategic recommendations to improve customer retention.

## 📂 Dataset Information

**Dataset:** IBM Telco Customer Churn

| Description | Details |
|---|---|
| Total Records | 7,043 |
| Original Columns | 21 |
| Churned Customers | 1,869 |
| Retained Customers | 5,174 |
| Target Variable | Churn |

### Important Dataset Features

- `customerID` – Unique customer identifier
- `tenure` – Number of months with the company
- `Contract` – Customer contract type
- `PaymentMethod` – Customer payment method
- `MonthlyCharges` – Monthly subscription charges
- `TotalCharges` – Total amount charged
- `InternetService` – Internet service type
- `TechSupport` – Technical support availability
- `Churn` – Customer churn status

## 🛠️ Technologies Used

- **Python** – Data analysis and processing
- **Jupyter Notebook** – Interactive development environment
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Plotly** – Interactive visualizations
- **Git & GitHub** – Version control and project submission

## ⚙️ Project Workflow

### 1. Data Loading and Preprocessing
- Imported the IBM Telco Customer Churn dataset.
- Inspected dataset structure and data types.
- Checked missing values and duplicate records.
- Converted `TotalCharges` into numeric format.
- Handled 11 missing `TotalCharges` values.
- Created a numerical churn indicator.

### 2. Baseline Churn Analysis
Calculated overall churn and retention percentages.

**Formula:**

Churn Rate (%) = (Churned Customers / Total Customers) × 100

### 3. Customer Cohort Analysis
Grouped customers into six tenure categories:

- 0–12 Months
- 13–24 Months
- 25–36 Months
- 37–48 Months
- 49–60 Months
- 61–72 Months

Calculated customer retention and churn rates for each cohort.

### 4. Contract and Payment Analysis
- Compared churn across Month-to-Month, One-Year, and Two-Year contracts.
- Analyzed churn rates by payment method.
- Investigated customer retention patterns across contract categories.

### 5. High-Risk Customer Identification
- Analyzed monthly subscription charges.
- Identified Fiber Optic customers without technical support.
- Compared churn rates between customers with and without technical support.
- Investigated high-risk customer segments.

### 6. Data Visualization
Created visualizations to communicate analytical findings:

- Customer churn distribution.
- Cohort retention curve.
- Contract-wise churn analysis.
- Payment method churn analysis.
- Monthly charges churn analysis.
- Fiber Optic technical support comparison.
- Customer churn heatmap.

## 📈 Key Analytical Findings

| Analysis | Result |
|---|---:|
| Overall Churn Rate | 26.54% |
| Overall Retention Rate | 73.46% |
| Month-to-Month Churn | 42.71% |
| One-Year Contract Churn | 11.27% |
| Two-Year Contract Churn | 2.83% |
| Electronic Check Churn | 45.29% |
| High Monthly Charges Churn | 37.82% |
| Fiber Optic Without Tech Support Churn | 49.37% |

### Customer Retention Insights

- Customers with shorter subscription tenure show higher churn rates.
- Retention generally improves as customer tenure increases.
- Month-to-month contract customers have substantially higher churn.
- Electronic check users show the highest churn among payment methods.
- Fiber Optic customers without technical support represent an important high-risk segment.

## 💡 Strategic Retention Recommendations

1. **Improve Customer Onboarding:** Introduce welcome programs and regular follow-ups for new customers.
2. **Encourage Long-Term Contracts:** Provide discounts and loyalty benefits for annual subscriptions.
3. **Improve Payment Convenience:** Encourage automatic payment methods.
4. **Enhance Technical Support:** Provide better support services for Fiber Optic customers.
5. **Personalized Pricing:** Introduce suitable subscription plans for customers with higher monthly charges.
6. **Monitor High-Risk Customers:** Use customer segmentation to identify and proactively engage customers at risk of leaving.

## 📁 Project Structure

```text
Week-3-Customer-Cohort-Churn/
│
├── README.md
├── Customer_Cohort_Churn.ipynb
│
├── data/
│   └── telco_customer_churn.csv
│
├── reports/
│   ├── cohort_retention_summary.csv
│   ├── contract_churn_summary.csv
│   ├── payment_churn_summary.csv
│   └── churn_analysis_report.md
│
└── screenshots/
    ├── Customer_Churn_Distribution.png
    ├── Cohort_Retention.png
    ├── contract_churn.png
    ├── payment_churn.png
    └── churn_heatmap.png
```

## 🚀 How to Run This Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/Surya2006Jaya/Datheon_Data_Analytics_and_Power_BI_Internship.git
```

### Step 2: Navigate to the Project Folder

```bash
cd Datheon_Data_Analytics_and_Power_BI_Internship/Week-3-Customer-Cohort-Churn
```

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Run the Notebook

Open `Customer_Cohort_Churn.ipynb` and execute all cells sequentially.

## 📊 Expected Deliverables

- Complete Jupyter Notebook with Python code and outputs.
- Customer cohort retention matrix.
- Customer churn analysis report.
- Contract and payment method analysis reports.
- Customer churn heatmap.
- Data visualization screenshots.
- Strategic customer retention recommendations.

## 📝 Conclusion

The Customer Cohort & Churn Analytics project provides insights into customer retention patterns and churn behavior using Python-based data analysis.

By analyzing 7,043 telecom customer records, the project identifies high-risk customer segments and highlights the importance of customer engagement, contract optimization, convenient payment methods, and technical support.

The findings can help businesses develop data-driven retention strategies, reduce customer churn, and improve long-term customer relationships.

---

**Project:** Week 3 – Customer Cohort & Churn Analytics  
**Internship:** Data Analytics & Power BI Internship  
**Tools:** Python | Pandas | NumPy | Matplotlib | Seaborn | Jupyter Notebook