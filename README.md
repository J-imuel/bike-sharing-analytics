# 🚲 Bike Sharing Analytics Dashboard

## 📌 Overview

This project analyzes large-scale bike-sharing data to uncover usage patterns, rider behavior, and operational insights. The analysis focuses on identifying peak demand periods, understanding user segmentation, and optimizing resource allocation through data-driven decision-making.

---

## 🎯 Business Objective

The objective of this project is to support bike-sharing operations by:

* Identifying peak ride hours and high-demand days
* Understanding differences between **member and casual users**
* Analyzing ride duration patterns
* Providing actionable insights to improve efficiency and user retention

---

## 📊 Dashboard Preview

![Dashboard](images/dashboard_preview.png)

---

## 🗄️ Data Source

* Dataset: Bike-sharing trip data (2025)
* Total Records: **5.5+ million rides**

### Key Fields:

* Ride ID
* Start Timestamp
* Ride Duration
* User Type (Member / Casual)

---

## 🛠 Tools & Technologies

* **Google BigQuery** (SQL for data processing and aggregation)
* **Tableau** (Interactive dashboard and visualization)
* **Python (Optional)** (Data preprocessing)

---

## 🗄️ Data Processing (SQL - BigQuery)

Data transformation and aggregation were performed using SQL in Google BigQuery.

### Key Steps:

* Extracted **start hour** from timestamp
* Derived **day of week**
* Calculated **ride duration (minutes)**
* Aggregated ride counts for analysis

### Sample Query:

```sql
SELECT
  EXTRACT(HOUR FROM started_at) AS start_hour,
  COUNT(*) AS total_rides
FROM bike_data
GROUP BY start_hour
ORDER BY start_hour;
```

---

## 📈 Key Insights

### 🕒 Peak Usage Time

* Highest ride activity occurs between **4 PM – 6 PM**
* Indicates strong commuter and after-work demand

---

### 📅 Weekly Trends

* Ride volume increases toward the weekend
* **Saturday shows the highest activity**, suggesting leisure usage

---

### 👥 User Segmentation

* **Members:** 64%
* **Casual Users:** 36%
* Members exhibit more consistent usage patterns

---

### ⏱ Ride Duration

* Majority of rides fall within **0–15 minutes**
* Indicates short-distance, utility-based trips

---

## 📊 Dashboard Features

* KPI Cards:

  * Total Rides
  * Average Ride Length
  * Membership Distribution

* Visualizations:

  * Weekly Ride Distribution
  * Ride Start Time Analysis
  * Ride Duration Histogram
  * User Type Comparison

---

## 💼 Business Recommendations

* **Optimize Bike Availability**

  * Increase supply during peak hours (4–6 PM)

* **Target Casual Users**

  * Introduce incentives to convert casual riders into members

* **Improve Resource Allocation**

  * Focus operations on high-demand days (weekends)

* **Schedule Maintenance Strategically**

  * Perform maintenance during low-usage periods

---

## ⚙️ How to Use

1. Download or clone the repository
2. Open the Tableau dashboard:

   * `dashboards/bike_dashboard.twbx`
3. Explore the dashboard to analyze usage patterns and insights

---

## 📁 Project Structure

```bash
bike-sharing-analytics/
│
├── dashboards/
│   └── bike_dashboard.twbx
│
├── images/
│   └── dashboard_preview.png
│
├── README.md
├── case_study.md
└── requirements.txt
```

---

## 📌 Key Takeaways

* Peak demand occurs during evening hours
* Weekend usage is significantly higher
* Majority of users are subscribed members
* Trips are predominantly short-duration

---

## 🚀 Future Improvements

* Integrate **weather data analysis**
* Develop **predictive models for demand forecasting**
* Build a **web-based interactive dashboard**

---

## 👤 Author

**Rey Jimuel Dimas**
Data Analyst | SQL | Tableau | BigQuery
