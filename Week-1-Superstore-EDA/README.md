# 📊 Week 1 – Exploratory Data Analysis on Superstore Retail Sales

> **Status:** ✅ **Completed** — *Datheon Data Analytics & Power BI Internship*

---

## 📌 Project Overview

This project focuses on conducting an in-depth **Exploratory Data Analysis (EDA)** on the **Superstore Retail Sales Dataset**. The primary objective is to evaluate retail sales performance, analyze customer purchasing behavior across segments, uncover monthly seasonality patterns, examine category-level revenue and profitability, and investigate the impact of discounting strategies on business profit margins.

The entire analysis is implemented in Python within a structured Jupyter Notebook, accompanied by high-resolution visual plots and executive business takeaways.

---

## 🎯 Key Project Objectives

- **Data Hygiene & Preprocessing:** Validate raw retail transactions, identify and handle missing attributes, eliminate anomalies, and extract temporal features (`Year`, `Month`, `Year-Month`).
- **Customer Purchase Volume Analysis:** Evaluate distribution of total sales, profit, and order volumes across Customer Segments (`Consumer`, `Corporate`, `Home Office`).
- **Monthly Sales Seasonality Analysis:** Trace sales fluctuations over the calendar timeline to isolate seasonal demand peaks and promotional spikes.
- **Category-Wise Revenue & Margin Analysis:** Compare performance across product categories (`Technology`, `Furniture`, `Office Supplies`) and evaluate whether high revenue corresponds to high profitability.
- **Discount Sensitivity Investigation:** Analyze how discounting ranges correlate with unit and total profit to detect profit erosion.
- **Regional Performance Evaluation:** Determine top and underperforming geographic sales regions (`West`, `East`, `Central`, `South`).
- **Executive Decision-Making Insights:** Formulate actionable, data-backed business takeaways for executive stakeholders.

---

## 📂 Dataset Information

- **Dataset File:** `data/superstore_sales.csv`
- **Total Orders Analyzed:** 5,009
- **Total Unique Customers:** 793
- **Total Sales Generated:** $2,297,200.86
- **Total Net Profit:** $286,397.02
- **Overall Profit Margin:** 12.47%

### Key Attributes
- `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`
- `Customer ID`, `Customer Name`, `Segment`
- `Country`, `City`, `State`, `Postal Code`, `Region`
- `Product ID`, `Category`, `Sub-Category`, `Product Name`
- `Sales`, `Quantity`, `Discount`, `Profit`

---

## 🛠️ Tools & Technologies Used

- **Python 3.10+**
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Development Environment:** Jupyter Notebook

---

## ⚙️ Analytical Workflow & Methodology

1. **Dataset Ingestion & Inspection:** Loaded 5,000+ transaction rows, audited data types, and confirmed row integrity.
2. **Missing Value Auditing:** Inspected and visualized null distribution using missing-value heatmaps (`reports/missing values.png`).
3. **Data Preprocessing & Feature Engineering:**
   - Standardized `Order Date` into ISO datetime format.
   - Extracted `Year`, `Month`, and `Year-Month` periodic periods.
4. **Segment Profiling:** Grouped sales and profit metrics by customer segment.
5. **Temporal Trend Analysis:** Aggregated monthly sales and profit timelines to identify sales seasonality (`reports/Monthly sales trend.png`).
6. **Category & Sub-Category Diagnostics:**
   - Evaluated revenue distribution (`reports/Revenue by Product Category.png`).
   - Evaluated net profit distribution (`reports/Profit by Product Category.png`).
7. **Discount Sensitivity Analysis:**
   - Evaluated correlation between discount tiers and profit erosion.
   - Identified average profit changes across discount brackets (`reports/Average Profit by Discount Level.png`).
8. **Geographical Performance Mapping:** Grouped regional revenues and profit contributions across West, East, Central, and South (`reports/Sales by Region.png`).

---

## 📈 Key Findings & Executive Takeaways

| Metric / Dimension | Observation | Executive Impact |
|---|---|---|
| **Top Customer Segment** | Consumer segment drives the majority of total sales and order count. | High volume driver; retention loyalty programs will safeguard core cash flow. |
| **Seasonality Peaks** | Q4 (September – December) consistently exhibits annual sales surges. | Inventory restocking and logistics scaling must be prioritized in late Q3. |
| **Category Dynamics** | `Technology` achieves the highest overall revenue and strong profit margins, while `Furniture` exhibits lower margins despite solid volume. | Re-evaluate furniture freight, handling, and manufacturer pricing agreements. |
| **Discount Sensitivity** | Discounts exceeding 20% lead to steep declines in net profitability, turning negative at high discount levels. | Enforce discount guardrails; shift sales incentives toward value-added bundles rather than margin-eroding discounts. |
| **Regional Sales** | The `West` and `East` regions outperform `Central` and `South` in both gross revenue and margin resilience. | Optimize logistics overhead and targeted promotional campaigns in underperforming territories. |

---

## 📁 Folder Structure

```text
Week-1-Superstore-EDA/
│
├── README.md                      # Detailed Week 1 documentation
├── Superstore_EDA.ipynb           # Executed Jupyter notebook with outputs
│
├── data/
│   └── superstore_sales.csv       # Retail sales transaction dataset
│
└── reports/
    ├── Average Profit by Discount Level.png
    ├── missing values.png
    ├── Monthly sales trend.png
    ├── Profit by Product Category.png
    ├── Revenue by Product Category.png
    ├── sales by customer segment.png
    └── Sales by Region.png
```

---

## 🚀 How to Run the Notebook

1. Ensure the repository dependencies are installed:
   ```bash
   pip install -r ../requirements.txt
   ```
2. Launch Jupyter Notebook from this folder:
   ```bash
   jupyter notebook Superstore_EDA.ipynb
   ```
3. Run all cells sequentially to reproduce figures and calculations.
