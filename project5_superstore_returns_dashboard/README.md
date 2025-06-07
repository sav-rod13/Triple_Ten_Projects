# 🔁 Superstore Returns Analysis – Storytelling with Data

## 📘 Project Overview

This project investigates the root causes of product returns at the Superstore and provides data-driven recommendations to reduce return volume. Using Tableau, I explored return behavior across multiple dimensions and delivered insights in the form of a **narrative Tableau Story** targeted at executive stakeholders.

The final product includes:
- An interactive Tableau dashboard
- A guided Story layout
- Strategic business recommendations

---

## 📊 Dashboard Link

🔗 [View the Tableau Story on Tableau Public](https://public.tableau.com/app/profile/savannah.rodriguez1156/viz/SavingSuperStore-SavannahRodriguezStorytelling/ReturnStoryDashboard?publish=yess)


---

## 📦 Dataset Used

**File:** `Superstore.xls`

Includes:
- `Orders` — sales data, products, customers, regions
- `Returns` — returned order IDs

---

## 🎯 Objective

Help the CEO and leadership team understand *what’s driving product returns*, where and when they happen most, and how to take action. The project follows a structured data storytelling arc, exploring geography, seasonality, product trends, and customer behavior.

---

## 🧪 Return Rate Analysis Approach

### Data Prep:
- Merged `Returns` and `Orders` via a **LEFT JOIN** on order ID.
- Created a calculated return flag:
  ```text
  IFNULL([Returned], "No") = "Yes" → 1, else 0
  ```
- Computed **Return Rate** as the average of this flag per segment (category, state, customer, etc.).

---

## 📚 Story Points Summary

1. **Where Are Returns Coming From?**  
   A U.S. map visualizing geographic return rates by state.

2. **When Are Returns Peaking?**  
   A time series line chart showing seasonal spikes, especially post-holiday.

3. **What’s Getting Returned?**  
   A composite view of return rate by product subcategory and geography.

4. **Who Is Returning the Most?**  
   Identified high-return-rate customers (filtered to those with >1 order).

5. **Root Cause Summary & Recommendations**  
   Final slide with actionable takeaways:
   - Improve quality control in high-return regions
   - Rethink policies for high-risk categories
   - Target customer support to heavy returners

---

## 📈 KPIs Tracked

- **Total Returns**
- **Total Orders**
- **Return Rate (%)**
- **Avg Profit vs Return Rate** (by various dimensions)

---

## 🛠 Tools Used

- Tableau Desktop + Public
- Excel (data prep)
- Markdown for documentation

---


