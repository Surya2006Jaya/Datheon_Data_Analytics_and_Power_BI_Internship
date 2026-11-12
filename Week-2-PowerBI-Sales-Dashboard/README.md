# 📊 Week 2 – Power BI Executive Sales & Profit Dashboard

> **Status:** ✅ **Completed** — *Datheon Data Analytics & Power BI Internship*

---

## 📌 Project Overview

This project focuses on transforming raw transactional retail sales data into a high-impact, interactive **Executive Sales & Profit Dashboard** built with **Microsoft Power BI Desktop**.

The dashboard empowers executive leadership, regional managers, and product planners to monitor organizational KPIs in real time, evaluate multi-year sales and profit trends, diagnose product line margins, and pinpoint geographical expansion opportunities.

---

## 🎯 Key Project Objectives

- **Enterprise Data Modeling:** Design a clean, scalable **Star Schema** with robust one-to-many (`1:*`) relationships between dimension and fact tables.
- **Power Query ETL:** Standardize data types, remove anomalies, handle null values, and structure date hierarchies.
- **DAX Formula Engineering:** Develop essential business intelligence metrics including Total Sales, Total Profit, Profit Margin %, Order Count, and Average Order Value.
- **Executive Visual Experience:** Build dynamic KPI cards, regional performance maps, category/sub-category profitability matrices, and monthly sales trend visuals.
- **Interactive Exploration:** Implement multi-level cross-filtering via slicers for Year, Region, Segment, and Product Category.
- **Executive Reporting:** Generate an official presentation-ready PDF report for executive reviews.

---

## 📂 Dataset & Artifact Information

- **Data File:** `data/superstore_sales.csv`
- **Dashboard File:** `Sales_Profit_Dashboard.pbix`
- **Executive Report:** `reports/Sales_Profit_Executive_Report.pdf`
- **Visual Previews:** `screenshots/`

---

## 🛠️ Tools & Technologies Used

- **Business Intelligence Platform:** Microsoft Power BI Desktop
- **Data Modeling & Calculations:** DAX (Data Analysis Expressions)
- **Data Transformation (ETL):** Power Query
- **Data Source:** CSV / Relational Flat File

---

## 📐 Data Architecture & Star Schema Model

The data model was architected to follow Kimball dimensional modeling principles:

- **Fact Table:**
  - `Fact_Orders` — Central transactional table storing `Order ID`, dates, keys, `Sales`, `Quantity`, `Discount`, and `Profit`.
- **Dimension Tables:**
  - `Dim_Customer` — Customer profiles (`Customer ID`, `Customer Name`, `Segment`).
  - `Dim_Product` — Product hierarchy (`Product ID`, `Category`, `Sub-Category`, `Product Name`).
  - `Dim_Geography` / `Dim_Region` — Location attributes (`Country`, `City`, `State`, `Postal Code`, `Region`).
  - `Dim_Date` — Continuous calendar dimension facilitating time-intelligence analysis.

*(See preview: [`screenshots/Data Model.png`](./screenshots/Data%20Model.png))*

---

## 🧮 Key DAX Measures Developed

```dax
// 1. Total Sales
Total Sales = SUM(Fact_Orders[Sales])

// 2. Total Profit
Total Profit = SUM(Fact_Orders[Profit])

// 3. Total Orders
Total Orders = DISTINCTCOUNT(Fact_Orders[Order ID])

// 4. Overall Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

// 5. Total Quantity Sold
Total Quantity = SUM(Fact_Orders[Quantity])

// 6. Average Order Value (AOV)
Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
```

---

## 📊 Dashboard Pages & Visual Highlights

### 1. Executive Overview Page
- **KPI Summary Cards:** Total Sales ($2.30M), Total Profit ($286.4K), Profit Margin (12.47%), Total Orders (5,009).
- **Monthly Revenue & Profit Seasonality:** Time-series line chart depicting end-of-year sales acceleration.
- **Regional Contribution Treemap:** West and East sales leadership comparison.
- **Customer Segment Breakdown:** Consumer (50%+ volume), Corporate (~30%), Home Office (~18%).

*(See preview: [`screenshots/Executive Overview.png`](./screenshots/Executive%20Overview.png))*

### 2. Product Profitability Page
- **Category Matrix:** Comparison of Technology, Furniture, and Office Supplies.
- **Top & Bottom Sub-Categories:** Identification of high-margin items (Copiers, Phones, Accessories) vs. loss-generating subcategories (Tables, Bookcases).
- **Discount Impact Analysis:** Visualizing the inverse relationship between aggressive discounts and gross profit.

*(See preview: [`screenshots/Product Profitability.png`](./screenshots/Product%20Profitability.png))*

---

## 📈 Strategic Business Insights

1. **Volume vs. Margin Disparity:** Technology generates both high sales volume and healthy profit margins; in contrast, Tables in the Furniture category generate consistent operating losses due to high freight costs and steep discounts.
2. **Promotional Discipline:** Orders with discounts greater than 20% severely erode net margin. Setting maximum regional discount thresholds will directly recover profitability.
3. **Territory Strength:** The West Region consistently delivers the highest net profit margin, serving as a regional benchmark for operational efficiency.

---

## 📁 Directory Structure

```text
Week-2-PowerBI-Sales-Dashboard/
│
├── README.md                                 # Week 2 project documentation
├── Sales_Profit_Dashboard.pbix               # Interactive Power BI dashboard
│
├── data/
│   └── superstore_sales.csv                  # Source retail dataset
│
├── reports/
│   └── Sales_Profit_Executive_Report.pdf     # Exported executive dashboard report
│
└── screenshots/
    ├── Data Model.png                        # Star Schema relationship diagram
    ├── Executive Overview.png                # Main KPI dashboard screenshot
    └── Product Profitability.png             # Product deep-dive analysis screenshot
```

---

## 🚀 How to Open and Explore the Dashboard

1. Install **Microsoft Power BI Desktop** (available free from the Microsoft Store).
2. Open [`Sales_Profit_Dashboard.pbix`](./Sales_Profit_Dashboard.pbix).
3. If prompted to update the data source path, point Power Query to [`data/superstore_sales.csv`](./data/superstore_sales.csv).
4. Use the interactive slicers on each page to filter by year, segment, or region.
