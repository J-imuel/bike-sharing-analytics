# 🚲 Bike Sharing Analytics Case Study

## 📌 1. Business Problem

Bike-sharing companies aim to optimize operations, improve customer retention, and maximize system usage. Achieving this requires a clear understanding of rider behavior and demand patterns.

### Key Questions:

* When are peak ride hours?
* How does usage vary across days of the week?
* What differences exist between **member and casual users**?
* What are the typical ride durations?

---

## 🎯 2. Business Objective

The goal of this analysis is to:

* Identify peak demand periods
* Understand user behavior and segmentation
* Analyze ride duration trends
* Provide actionable insights for operational efficiency

---

## 📊 3. Data Source

* Dataset: Bike-sharing trip data (2025)
* Total Records: **5.5+ million rides**

### Key Fields:

* Ride ID
* Start Timestamp
* Ride Duration
* User Type (Member / Casual)

---

## 🗄️ 4. Data Processing (SQL - BigQuery)

Data transformation and aggregation were performed using **Google BigQuery (SQL)**.

### Key Steps:

* Extracted **start hour** from timestamps
* Derived **day of the week**
* Calculated ride duration in minutes
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

## 📈 5. Data Analysis & Visualization

An interactive dashboard was developed in **Tableau** to present key insights.

### Key Metrics:

* Total Rides: **5.55M**
* Average Ride Length: **14.53 minutes**
* Membership Distribution: **64% Members / 36% Casual**

### Visualizations:

* Weekly Ride Distribution
* Ride Start Time Distribution
* Ride Duration Histogram
* User Type Comparison

---

## 🔍 6. Key Insights

### 🕒 Peak Ride Time

* Highest usage occurs between **4 PM – 6 PM**
* Indicates strong commuter and after-work demand

---

### 📅 Weekly Trends

* Ride volume increases toward the weekend
* **Saturday shows the highest activity**, suggesting leisure usage

---

### 👥 User Segmentation

* Members account for **64% of total rides**
* Casual users represent **36%**
* Members exhibit more consistent usage patterns

---

### ⏱ Ride Duration

* Most rides fall within **0–15 minutes**
* Suggests short-distance, utility-based trips

---

## 💼 7. Business Recommendations

### 🚲 Optimize Bike Availability

* Increase bike supply during **peak hours (4–6 PM)**

### 🎯 Convert Casual Users

* Introduce promotions or incentives to encourage membership

### 📍 Improve Resource Allocation

* Focus operations on **high-demand days (weekends)**

### 🔧 Schedule Maintenance Efficiently

* Perform maintenance during **low-demand hours**

---

## 🚀 8. Conclusion

This analysis highlights key behavioral patterns and demand trends in bike-sharing systems. By leveraging these insights, organizations can improve operational efficiency, enhance user experience, and drive membership growth.

---

## 📌 9. Limitations

* Dataset limited to a single year
* No geographic data included
* External factors (e.g., weather, events) not considered

---

## 🔮 10. Future Work

* Integrate **weather and location data**
* Develop **predictive models for demand forecasting**
* Build a **real-time analytics dashboard**

---

## 👤 Author

**Rey Jimuel Dimas**
Data Analyst | SQL | Tableau | BigQuery
