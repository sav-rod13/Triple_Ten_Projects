# 📈 Shopify Funnel Retention 

Welcome to my spreadsheet-based business analytics project for an e-commerce company. This case study simulates a real-world junior data analyst role, where I worked with raw website event logs to uncover business insights, build a conversion funnel, and conduct a full cohort retention analysis.

---

## 🧩 Project Objective

**Business Goal:**  
Help an e-commerce company understand:
- How users move through the purchase funnel
- Which users convert over time
- How user retention changes across acquisition cohorts

This analysis guides the company in improving conversion rates and customer retention strategies.

---

## 📁 Dataset Overview

The primary dataset, located in the `raw_user_activity` sheet, includes user-level website behavior:

| Column Name       | Description                                 |
|-------------------|---------------------------------------------|
| `user_id`         | Unique identifier for each customer         |
| `event_type`      | Type of activity (e.g. view, cart, purchase)|
| `category_code`   | Product category                            |
| `brand`           | Product brand                               |
| `price`           | Price in USD                                |
| `event_date`      | Date of the activity (YYYY-MM-DD)           |

---

## 🚦 Part 1: Conversion Funnel Analysis

Built a **3-stage conversion funnel** using pivot tables:

1. Product Page Views
2. Shopping Cart Views
3. Purchases

### Key Deliverables:
- Counted **unique users** at each funnel stage
- Calculated:
  - **Total Conversion Rate**
  - **Stage-to-Stage Conversion Rate**
- Sheet: `conversion_funnel`

---

## 📊 Part 2: Cohort Data Preparation

Isolated **purchase events** and structured data for cohort analysis:

- Created a sheet called `purchase_activity` to store only purchase rows
- Calculated each user’s **first purchase date** using pivot tables (`first_purchase` sheet)
- Added new columns:
  - `first_purchase_date` (via `VLOOKUP`)
  - `event_month` and `first_purchase_month` (via `TEXT`)
  - `cohort_age` (via `DATEDIF` in months)

---

## 📆 Part 3: Retention Cohort Analysis

Grouped users into **monthly cohorts** and tracked user activity over time:

- Created a pivot table in the `cohort_analysis` sheet
  - Rows: Cohort month (based on first purchase)
  - Columns: `cohort_age` (0–4 months)
  - Values: Unique users active each month

### Calculated Retention Rates
- Built a `retention_rates` sheet
- For each cohort and age (months 1–4), calculated:
  - **Retention rate = (active users at month n) / (initial cohort size)**
- Used fixed column referencing to copy formulas across the table

---

## 📝 Part 4: Executive Summary & Polish

Created an `Executive Summary` to clearly explain:

- Results:
  - Funnel conversion drop-offs
  - Highest converting stage
  - Overall retention trends across cohorts
- Analysis:
  - Data timeline, assumptions, and logic used
  - Details on how conversions and retention were calculated

Formatted the entire workbook for professional presentation:
- Bold headers, frozen rows, borders, clean date/number formats
- Organized tabs with a `Table of Contents` sheet up front

---

## 🛠️ Tools Used

- Google Sheets
- Pivot Tables
- VLOOKUP, TEXT, DATEDIF, IF
- Spreadsheet formatting best practices

---

## 📫 Contact

For questions, collaborations, or spreadsheet wizardry — let’s connect on [LinkedIn](https://www.linkedin.com) or GitHub!

---
