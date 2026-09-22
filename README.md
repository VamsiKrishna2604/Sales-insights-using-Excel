# Retail Sales Performance & Revenue Insights Dashboard

An interactive business intelligence dashboard developed entirely in **Microsoft Excel** to evaluate multi-year sales performance, regional demand trends, and product-line volume across 9,800 retail orders.

---

## 📌 Project Overview
This project transforms raw retail transactional records into a multi-tiered analytical workbook. By structuring data through lookup modeling, calculated fields, dynamic Pivot Tables, and interactive slicers, it demonstrates practical business intelligence, reporting, and data storytelling without requiring external BI software.

---

## 📁 Dataset Overview

The dataset contains **9,800 records** spanning 4 years (2015–2018) with a cumulative transaction value of **$2.26M+**.

* **Orders:** `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`
* **Customers:** `Customer ID`, `Customer Name`, `Segment` (Consumer, Corporate, Home Office), `Country`, `City`, `State`, `Postal Code`, `Region`
* **Products:** `Product ID`, `Category` (Furniture, Office Supplies, Technology), `Sub-Category` (17 lines), `Product Name`, `Sales`

### Engineered Helper Attributes
To support time-series evaluation and categorical drill-downs, the cleaned dataset incorporates 7 custom fields:
* `Order year` & `Order month`: Extracted from order dates for seasonal and YoY trending.
* `Customer ID prefix`: Segment classification derived via text parsing.
* `Rank`: Revenue ranking across individual orders.
* `Total Sales`, `Average sales`, `Largest sale`: Benchmark baseline calculations for quick-ratio analysis.

---

## 🛠 Tools & Techniques Used

* **Workbook Structure:** 3-tier modular architecture (`Cleaned Data`, `Analysis`, `Dashboard`).
* **Formulas & Modeling:** Lookup logic (`XLOOKUP`, `INDEX/MATCH`), date functions (`YEAR`, `MONTH`), text manipulation (`LEFT`), and statistical ranking (`RANK`).
* **Aggregation:** Multi-dimensional Pivot Tables and summary aggregation tables.
* **Interactivity:** Multi-criteria Slicers (`Region`, `Year`) connected across charts and KPI scorecards.
* **Visual Formatting:** Automated conditional formatting rules to highlight high-value sales (> $1,000) and identify top/bottom volume drivers.

---

## 📈 Dashboard Architecture & Features

### 1. Executive KPI Scorecards
* **Total Sales:** $2,261,536.78
* **Total Transactions:** 9,800 orders
* **Average Yearly Revenue:** ~$565,834
* **Top Performing Region:** West (highest transaction volume and gross revenue)

### 2. Territory & Customer Distribution
* Cross-tabulated sales distribution across 4 geographic regions (Central, East, South, West) segmented by Consumer, Corporate, and Home Office demand.
* Interactive slicer controls allowing immediate filtering by operational territory and fiscal year.

### 3. Category & Temporal Trends
* Monthly trend tracking mapping revenue surges throughout the financial year.
* Volume analysis across 3 primary categories and 17 distinct sub-categories.
* Identification of top-grossing individual SKUs via dedicated lookup and ranking tables.

---

## 🔍 Key Business Insights

* **Regional Dominance:** The **West** region leads all territories in both transaction volume (3,140 orders) and revenue ($710,219), followed by the **East** ($669,518). Together, these two territories contribute **over 61% of total business revenue**.
* **Category Dynamics:** While **Technology** accounted for the largest revenue share ($827,455), **Office Supplies** generated the vast majority of transactional volume (5,909 orders).
* **Revenue Concentration:** Top-tier revenue is concentrated heavily in enterprise office equipment, led by the **Canon imageCLASS 2200 Advanced Copier** ($61,599 in sales) alongside commercial binding and print machines.
* **Seasonality Trends:** Sales consistently ramp up in Q3 and peak in Q4, with **November ($350K+)** and **December ($321K+)** exhibiting the highest seasonal demand.
