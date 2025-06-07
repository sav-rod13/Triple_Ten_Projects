# 🏙️ Manhattan Airbnb Investment Analysis

Welcome to my spreadsheet-based data analysis project exploring the **Manhattan vacation rental market** using Airbnb listings and calendar data. This analysis was conducted to help a client make informed investment decisions on the most profitable neighborhoods and property types for short-term rentals.

---

## 📊 Project Overview

**Client Goal:**  
Identify which neighborhoods and property sizes are most attractive and profitable for vacation rentals in Manhattan, based on publicly available Airbnb data.

---

## 🔍 Key Questions Answered

1. **Which neighborhoods and property sizes are most attractive for vacation rentals?**
2. **How much money did these top listings generate?**

---

## 🧹 Data Cleaning Summary

Detailed cleaning steps are included in a dedicated `Change Log` sheet. Key highlights include:

- Created `neighborhood_clean` column: Standardized inconsistent casing and removed trailing spaces from the neighborhood field.
- Created `bedrooms_clean` column: Replaced blanks with `0` to represent studio apartments.
- Created `top_listing` column: Flagged listings that matched top neighborhood + optimal bedroom combinations.
- Created `revenue_earned` columns in both listings and calendar sheets to estimate revenue from adjusted prices.
- Used `SUMIF()` to consolidate daily revenue from calendar data to listing-level aggregates.

---

## 📌 Data Sources

- [NYC Airbnb Open Data (Inside Airbnb)](http://insideairbnb.com/get-the-data.html)  
- Provided project brief and spreadsheets including:
  - `listings` (property metadata)
  - `calendar` (daily availability & pricing)

---

## 📈 Analysis Insights

### 🏘️ Top 10 Neighborhoods for Vacation Rentals
- Based on number of reviews in the last 12 months (`number_of_reviews_ltm`)
- Most attractive:  
  - **Hell's Kitchen**  
  - **Harlem**  
  - **Midtown**
- Visualized via bar chart with pivot table support

### 🛏️ Most Popular Property Sizes
- 1-bedroom apartments and studios dominate bookings
- Analyzed via cleaned `bedrooms_clean` column and property count

### 🧠 Neighborhood-Specific Preferences
- Most neighborhoods preferred **1-bedrooms**
- **Midtown** favored **studios**

### 💰 Revenue Estimation
- Daily revenue computed via `calendar[adjusted_price]` × occupancy
- Aggregated to 30-day and estimated annual revenue
- Top-earning listing ID: **49946551**
  - Estimated 30-day revenue: `$29,940`
  - Projected annual revenue: `$359,280`

---

## 📋 Final Deliverables

- ✅ Fully formatted and annotated Excel workbook
- ✅ Executive summary and table of contents
- ✅ Documented data cleaning steps (Change Log tab)
- ✅ Charts and pivot tables answering all business questions
- ✅ Clear assumptions and consistent formatting throughout

---

## 📎 Recommendations

Based on the findings:
- Invest in **1-bedroom properties** across top neighborhoods
- Consider **studio apartments** in **Midtown**
- Focus on areas with consistently high review volumes (as a proxy for demand)
- Prioritize listings with higher occupancy and nightly rates for max ROI

---

## 🧠 Tools Used

- Microsoft Excel  
- Pivot Tables  
- IF(), SUMIF(), and other formula-based logic  
- Manual and formula-driven data cleaning

---

