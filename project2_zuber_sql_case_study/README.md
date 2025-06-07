# 🚕 Zuber SQL Analysis Project

Welcome to the SQL analysis project for **Zuber**, a fictional ride-sharing startup entering the Chicago market. In this project, I explored real-world taxi data to identify usage patterns, evaluate competitor performance, and assess how weather affects rider behavior.

This case study simulates the role of a **data analyst** supporting business strategy and decision-making using SQL.

---

## 📊 Project Overview

**Company Objective:**  
Zuber is planning a launch in Chicago and needs insights into passenger behavior, external influences like weather, and competitor performance.

**Analytical Goals:**
1. Perform **exploratory data analysis** on taxi rides in November 2017.
2. Determine if **weather conditions** affect ride duration between key neighborhoods on Saturdays.

---

## 🗃️ Data Description

The analysis is based on four tables from a relational database:

### `neighborhoods`
| Column | Description               |
|--------|---------------------------|
| `name` | Neighborhood name         |
| `neighborhood_id` | Unique ID     |

### `cabs`
| Column | Description               |
|--------|---------------------------|
| `cab_id` | Vehicle code            |
| `vehicle_id` | Technical vehicle ID|
| `company_name` | Cab company       |

### `trips`
| Column | Description                          |
|--------|--------------------------------------|
| `trip_id` | Unique ride ID                    |
| `cab_id` | Cab used for the ride              |
| `start_ts`, `end_ts` | Start/end timestamps   |
| `duration_seconds` | Duration in seconds      |
| `distance_miles` | Distance traveled          |
| `pickup_location_id`, `dropoff_location_id` | Neighborhoods |

### `weather_records`
| Column | Description                           |
|--------|---------------------------------------|
| `ts` | Date and time of record (hourly)       |
| `temperature` | Temp at time of record         |
| `description` | Text weather description       |

---

## 🧭 Step 1: Exploratory Data Analysis

### ✅ Trips by Taxi Company (Nov 15–16, 2017)
- Aggregated total trips per company
- Sorted results by most active companies
- Output field: `trips_amount`

### ✅ Companies with "Yellow" or "Blue" in Name (Nov 1–7)
- Used `LIKE '%Yellow%' OR '%Blue%'`
- Grouped by `company_name`

### ✅ Popularity Breakdown (Nov 2017)
- Compared **Flash Cab** and **Taxi Affiliation Services**
- All other companies grouped as `"Other"`
- Output sorted by `trips_amount`

---

## 🌧️ Step 2: Weather & Ride Duration

### ✅ Weather Condition Classification
- Used `CASE` to classify each hourly weather record:
  - `"Bad"` if `description` contained `"rain"` or `"storm"`
  - `"Good"` otherwise
- Output: `ts` and `weather_conditions`

### ✅ Rides from Loop → O’Hare on Saturdays
- Retrieved rides **starting in the Loop (ID: 50)** and ending at **O’Hare (ID: 63)**
- Filtered to **Saturdays only**
- Joined with weather data on the `start_ts = ts` key
- Compared `duration_seconds` for `"Bad"` vs `"Good"` conditions

---

## 💡 Key Insights

- Identified **top-performing taxi companies** on key November dates
- Found meaningful patterns in **company name popularity**
- Highlighted impact of **weather on ride duration** for strategic airport routes

---

## 🧠 Skills Demonstrated

- Complex SQL JOINs
- Subqueries & `CASE` logic
- Data cleaning and classification
- Date/time filtering
- Aggregation and grouping
- Hypothesis testing with real-world logic

---

## 🧰 Tools Used

- PostgreSQL
- SQL Management Tool (e.g., DBeaver, pgAdmin, etc.)
- Google Sheets (for formatting insights if exported)

---

## 📫 Contact

Questions or feedback? Let’s connect on [LinkedIn](https://www.linkedin.com) or GitHub!

---

