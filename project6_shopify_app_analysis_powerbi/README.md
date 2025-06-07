# 📊 Shopify App Store Analysis – Power BI Project

Welcome to my Power BI project focused on analyzing data from the Shopify App Store. As a business intelligence consultant, I was hired to explore public app data and uncover patterns around app success, user reviews, and developer responsiveness.

This analysis was completed using Microsoft Power BI and is structured into three interactive report pages, aligned with the business questions provided.

---

## 📁 Dataset

**File:** `shopify.xlsx`  
Contains four tables scraped from public Shopify listings:

| Table             | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `apps`           | App metadata (name, developer, rating, review count, last modified date)   |
| `apps_categories`| Bridge table linking apps to categories                                     |
| `categories`     | List of app categories                                                      |
| `reviews`        | User reviews, ratings, and developer responses                              |

---

## 🧩 Project Objective

Help Shopify stakeholders understand:
- Where the app marketplace is thriving (and failing)
- Which developers are most engaged
- What trends drive successful app performance

---

## 📊 Report Sections

---

### 🟩 **Part 1: App Landscape**

**Report Page:** `App Landscape`

| Visual | Description |
|--------|-------------|
| ✅ KPI Card | Total number of unique apps |
| ✅ Line Chart | Total review volume over time (X: `lastmod`, Y: `sum of reviews_count`) |
| ✅ Scatterplot | Review count vs. average rating for each app (with interpretation text box) |

---

### 🟦 **Part 2: Reviews**

**Report Page:** `Reviews`

| Visual | Description |
|--------|-------------|
| ✅ Card | Average of new calculated column: `helpful_reviews = rating * (1 + helpful_count)` |
| ✅ Scatterplot | X: `developer_answered` (0 or 1), Y: `average rating` (one point per group) |
| ✅ DAX Columns |
```DAX
helpful_reviews = reviews[rating] * (1 + reviews[helpful_count])

developer_answered = IF(ISBLANK(reviews[developer_reply]), 0, 1)
