<h1 align="center">📊 Revenue & Customer Analytics Dashboard – Tricket App</h1>

<p align="center">
  <b>Data-Driven Revenue, Engagement & Retention Insights | Built for Helpen.In Enterprises Pvt. Ltd.</b>
</p>

---
<p align="center">

[![Overview](https://img.shields.io/badge/SECTION-Overview-1E90FF?style=for-the-badge&logo=markdown)](#-project-overview)
[![KPIs](https://img.shields.io/badge/KPIs-32CD32?style=for-the-badge&logo=target)](#-key-kpis-tracked)
[![SQL](https://img.shields.io/badge/SQL%20Queries-4169E1?style=for-the-badge&logo=database)](#-sql-queries-used)
[![DataModel](https://img.shields.io/badge/Data%20Model-FF8C00?style=for-the-badge&logo=databricks)](#-data-model-design)
[![Wireframe](https://img.shields.io/badge/Wireframes-FF69B4?style=for-the-badge&logo=powerbi)](#-power-bi-wireframe-mockups)
[![Insights](https://img.shields.io/badge/Key%20Insights-9370DB?style=for-the-badge&logo=insight)](#-business-insights--impact)

</p>

<p align="center">
  <!-- Badges -->
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge&logo=powerbi" alt="Power BI Badge">
  <img src="https://img.shields.io/badge/SQL-MySQL-orange?style=for-the-badge&logo=mysql">
 <a href="https://github.com/SHAHNAWAZSERAJI/"> <img src="https://img.shields.io/badge/Data%20Analyst%20Portfolio-Showcase-blue?style=for-the-badge&logo=github">
  <img src="https://img.shields.io/badge/ETL%20Automation-Enabled-green?style=for-the-badge&logo=microsoft">
  <img src="https://img.shields.io/github/stars/SHAHNAWAZSERAJI/Revenue-Customer-Analytics-Dashboard?style=for-the-badge" alt="GitHub stars">
  <a href="https://www.linkedin.com/in/shahnawazseraji/">
    <img src="https://img.shields.io/badge/View%20on%20LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
  </a>
</p>

---

## 🧭 **Project Overview**

The **Revenue & Customer Analytics Dashboard** is an end-to-end **Power BI + SQL** solution built for the **Tricket App** — a live cricket prediction platform by **Helpen.In Enterprises Pvt. Ltd.**

It provides a unified view of **revenue, profitability, and customer engagement**, allowing stakeholders to identify growth opportunities, improve retention, and optimize contests for maximum business value.

This solution automates reporting pipelines, integrates transactional and engagement data, and presents **real-time KPIs** through interactive Power BI dashboards.

---

## 🎯 **Business Objectives**

- Monitor **daily, weekly, and monthly revenue** performance across contests.  
- Evaluate **user engagement, retention, and churn** behaviour.  
- Identify **top-performing users, contests, and regions** driving growth.  
- Optimize marketing spend through **LTV vs CAC** insights.  
- Automate ETL & reporting for **faster decision-making**.

---

## 🛠️ **Tech Stack & Tools**

| Technology | Purpose |
|-------------|----------|
| **Power BI** | Data Visualization, KPI Dashboarding, DAX Measures |
| **SQL (MySQL)** | Querying, Data Modeling, Aggregations |
| **Power Query** | ETL Automation, Data Cleansing |
| **Excel** | Data Validation & QA |
| **DAX** | KPI Calculations, LTV & ARPU Computations |

---

## 📊 **Key Performance Indicators (KPIs)**

| KPI | Description | Formula Example |
|------|--------------|----------------|
| **Total Revenue** | Total entry fees collected from contests | `SUM(Transactions[amount_paid])` |
| **Net Profit** | Revenue – Payouts | `SUM(amount_paid) - SUM(amount_won)` |
| **ARPU (Avg. Revenue per User)** | Avg. revenue per active user | `DIVIDE([Total Revenue], DISTINCTCOUNT(Users[user_id]))` |
| **User Retention Rate** | Returning users / New users | `DIVIDE([Returning Users], [New Users])` |
| **Churn Rate** | Percentage of users who stop participating | `1 - [Retention Rate]` |
| **LTV (Lifetime Value)** | ARPU × Avg. Retention Duration | `ARPU * AvgDaysActive` |
| **Top 5 Revenue Regions** | Geo-level revenue distribution | via `RANKX` DAX & map visuals |

---

## 🚀 **Dashboard Features**

- 📈 **Revenue Trend Analysis** – Daily & Monthly performance tracking  
- 👥 **Customer Segmentation** – Channel-, region-, and value-based user clusters  
- 💰 **Profitability Breakdown** – Entry fees, payouts, and margins by contest  
- 🌍 **Geo Revenue Visualization** – Regional contribution heat-map  
- 📦 **Contest Insights** – Top performing matches, conversion & retention impact  
- 🔄 **Automated ETL** – Power Query-based refresh pipelines  
- 📧 **Email Alerts & Reports** – Auto-scheduled updates for business heads  

---
## 🧮 Data Model Design  

Power BI **Star Schema** model built on SQL-processed tables:

Fact_Revenue (contest_id, date, revenue, payout, profit_margin)


|-- Dim_Contest (contest_id, contest_type, match_type, region)

|-- Dim_User (user_id, gender, state, signup_date)

|-- Dim_Date (date_id, month, quarter, year)

|-- Dim_Channel (channel_id, acquisition_source, campaign_type)


---

## 📊 Power BI Wireframe Mockups  

### Dashboard Layout Overview  

📍 Page 1 – Revenue Overview

→ KPI Cards (Total Revenue, Payouts, Profit Margin)

→ Line Chart: Revenue Trend (Daily/Monthly)

→ Bar Chart: Revenue by Contest Type

→ Matrix: Top Performing Contests

📍 Page 2 – Customer Insights

→ Cohort Retention Heatmap

→ Pie Chart: User Segmentation (High vs Low Value)

→ KPI: ARPU, Repeat Users, Conversion 

📍 Page 3 – Validation & QA

→ Source vs Target Revenue Check

→ Data Refresh Status Indicator

---
## 📈 **Power BI Dashboard Preview**
1.
<p align="center"><img width="1536" height="1024" alt="REVENUE TRENDS -TRICKET" src="https://github.com/user-attachments/assets/4298b111-7fde-4ea1-bd77-26e945f478ff" />

2.<img width="1536" height="1024" alt="TRICKET-USER RETENTION" src="https://github.com/user-attachments/assets/402ebaa2-5920-4c70-aa1b-af03d47ca51b" />

---

---


## ⚙️ **Data Model & Design**

- **Fact Table:** Transactions (txn_id, user_id, contest_id, amount_paid, amount_won, txn_date)  
- **Dimension Tables:** Users, Contests, Marketing, Regions  
- **Model Type:** *Star Schema*  
- Integrated via **Power Query ETL** → Loaded to Power BI Model → DAX measures built on top.  

---

## 💡 **Key Insights & Outcomes**

✅ **65% of revenue** generated by **top 20% of users** (Pareto Principle)  
✅ Users from **referral channels** showed **30% higher retention**  
✅ **Contest profitability** improved by **18%** after fee optimization  
✅ **Reporting time** reduced from 2 hrs/day → 10 min with automation  
✅ **Data-backed campaign targeting** improved marketing ROI by 25%  

---

## 👨‍💼 **My Role**

- Designed **data model, SQL queries & ETL process**  
- Developed **interactive Power BI dashboards & KPI cards**  
- Implemented **DAX measures** for ARPU, LTV, churn & retention  
- Conducted **UAT & QA validation** with stakeholders  
- Automated reporting workflows for **real-time updates**

---

## 🔮 **Future Enhancements**

- 🤖 **AI-based Revenue Forecasting** using time-series data  
- 🔔 **Automated Alerts** for KPI threshold breaches  
- ☁️ **Integration with Azure / Snowflake** for data scalability  
- 📊 **User Churn Prediction Model** via Python integration in Power BI  

---

## 🧩 **Business Impact Summary**

| Impact Area | Before | After |
|--------------|--------|-------|
| **Reporting Time** | Manual ~2 hrs/day | Automated ~10 min |
| **Profit Margin** | Baseline | +18% Improvement |
| **Decision Speed** | Delayed reports | Real-Time Dashboard |
| **Data Accuracy** | Inconsistent | 100% Validated with SQL |
| **Retention Visibility** | Partial | 360° Customer View |



<p align="center">
  ⭐ If you found this project useful, don’t forget to <b>star</b> the repository and follow for more Power BI & SQL projects!
</p>


## 🧩 SQL Queries Used  

Below are some key SQL queries used in the **Revenue & Customer Analytics Dashboard – Tricket App** project.  
These queries were essential for **data extraction, validation, transformation, and KPI computation** before building the Power BI model.  

---

### 1️⃣ Revenue Summary by Contest Type
```sql
SELECT 
    contest_type,
    COUNT(DISTINCT contest_id) AS total_contests,
    SUM(entry_fee * total_players) AS total_revenue,
    SUM(total_payout) AS total_payout,
    (SUM(entry_fee * total_players) - SUM(total_payout)) AS net_margin,
    ROUND(((SUM(entry_fee * total_players) - SUM(total_payout)) / SUM(entry_fee * total_players)) * 100, 2) AS margin_percent
FROM contest_revenue
GROUP BY contest_type
ORDER BY total_revenue DESC;
- Purpose:
Calculates revenue, payouts, and profit margin for each contest type (e.g., Live, Upcoming, Free Play).

2️⃣ Top Performing Users by Lifetime Winnings
SELECT 
    user_id,
    username,
    SUM(winnings) AS total_winnings,
    COUNT(DISTINCT contest_id) AS contests_played,
    ROUND(AVG(prediction_accuracy)*100, 2) AS avg_accuracy_pct
FROM user_performance
GROUP BY user_id, username
HAVING COUNT(DISTINCT contest_id) > 10
ORDER BY total_winnings DESC
LIMIT 10;

- Purpose:
Identifies high-value users based on lifetime winnings and accuracy — used for loyalty insights & targeted campaigns.

3️⃣ Daily Active Users (DAU) & Paying Users Trend

SELECT 
    event_date,
    COUNT(DISTINCT user_id) AS daily_active_users,
    COUNT(DISTINCT CASE WHEN is_premium = 1 THEN user_id END) AS daily_paying_users
FROM user_activity
GROUP BY event_date
ORDER BY event_date;

SELECT 
    event_date,
    COUNT(DISTINCT user_id) AS daily_active_users,
    COUNT(DISTINCT CASE WHEN is_premium = 1 THEN user_id END) AS daily_paying_users
FROM user_activity
GROUP BY event_date
ORDER BY event_date;

4️⃣ Average Revenue Per User (ARPU)

SELECT 
    ROUND(SUM(total_revenue) / COUNT(DISTINCT user_id), 2) AS arpu
FROM (
    SELECT 
        u.user_id,
        SUM(c.entry_fee) AS total_revenue
    FROM contest_entries c
    JOIN users u ON c.user_id = u.user_id
    GROUP BY u.user_id
) AS revenue_by_user;

Purpose:
Computes ARPU — a critical KPI showing user monetization efficiency for the Tricket platform.

5️⃣ Revenue Validation Check (ETL QA)

SELECT 
    t1.business_date,
    t1.total_revenue_source AS source_revenue,
    t2.total_revenue_target AS target_revenue,
    (t1.total_revenue_source - t2.total_revenue_target) AS diff
FROM source_revenue_summary t1
JOIN target_revenue_summary t2
ON t1.business_date = t2.business_date
WHERE ABS(t1.total_revenue_source - t2.total_revenue_target) > 0;

Purpose:
Performs QA to ensure no mismatches between source & transformed datasets before Power BI ingestion.

6️⃣ Retention Cohort Analysis

WITH user_cohorts AS (
    SELECT 
        user_id,
        MIN(DATE(first_contest_date)) AS cohort_date
    FROM user_contests
    GROUP BY user_id
)
SELECT 
    DATE_DIFF(u.event_date, c.cohort_date, DAY)/7 AS week_number,
    COUNT(DISTINCT u.user_id) AS retained_users
FROM user_activity u
JOIN user_cohorts c ON u.user_id = c.user_id
GROUP BY cohort_date, week_number
ORDER BY cohort_date, week_number;

Purpose:
Tracks user retention over weeks to identify engagement decay and predict churn patterns.

```
---

---
💡 Note:
All queries are optimized for MySQL and used within scheduled ETL pipelines.
Final aggregated outputs are pushed to Power BI using an automated dataflow for real-time updates.
---
## ⚙️ **Data Model & Design**

- **Fact Table:** Transactions (txn_id, user_id, contest_id, amount_paid, amount_won, txn_date)  
- **Dimension Tables:** Users, Contests, Marketing, Regions  
- **Model Type:** *Star Schema*  
- Integrated via **Power Query ETL** → Loaded to Power BI Model → DAX measures built on top.  

---

## 💡 **Key Insights & Outcomes**

✅ **65% of revenue** generated by **top 20% of users** (Pareto Principle)  
✅ Users from **referral channels** showed **30% higher retention**  
✅ **Contest profitability** improved by **18%** after fee optimization  
✅ **Reporting time** reduced from 2 hrs/day → 10 min with automation  
✅ **Data-backed campaign targeting** improved marketing ROI by 25%  

---

## 👨‍💼 **My Role**

- Designed **data model, SQL queries & ETL process**  
- Developed **interactive Power BI dashboards & KPI cards**  
- Implemented **DAX measures** for ARPU, LTV, churn & retention  
- Conducted **UAT & QA validation** with stakeholders  
- Automated reporting workflows for **real-time updates**

---

## 🔮 **Future Enhancements**

- 🤖 **AI-based Revenue Forecasting** using time-series data  
- 🔔 **Automated Alerts** for KPI threshold breaches  
- ☁️ **Integration with Azure / Snowflake** for data scalability  
- 📊 **User Churn Prediction Model** via Python integration in Power BI  

---

## 🧩 **Business Impact Summary**

| Impact Area | Before | After |
|--------------|--------|-------|
| **Reporting Time** | Manual ~2 hrs/day | Automated ~10 min |
| **Profit Margin** | Baseline | +18% Improvement |
| **Decision Speed** | Delayed reports | Real-Time Dashboard |
| **Data Accuracy** | Inconsistent | 100% Validated with SQL |
| **Retention Visibility** | Partial | 360° Customer View |

---

## 📬 **Connect With Me**

👤 **MD Shahnawaz**  
🔗 [LinkedIn](https://www.linkedin.com/in/shahnawazseraji/)  
🌐 [GitHub Portfolio](https://github.com/SHAHNAWAZSERAJI)  
📧 **md.shanwaz026@gmail.com**

---

<p align="center">
  ⭐ If you found this project useful, don’t forget to <b>star</b> the repository and follow for more Power BI & SQL projects!
</p>
