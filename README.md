# Beverage Sales & Workforce Analytics Dashboard

A multi-page enterprise Power BI dashboard solution bridging the gap between commercial sales performance and internal workforce dynamics.

---

## 📌 Executive Summary

Modern enterprise decisions require a holistic view of operations. This project solves a key business challenge for a growing enterprise: **the lack of unified visibility connecting regional sales metrics with internal human resources dynamics**. 

By consolidating disparate multi-departmental datasets—covering district sales performance, beverage brand breakdown, employee retention, satisfaction, and compensation—this Power BI project delivers a centralized reporting platform for executive leadership to evaluate commercial output and workforce health simultaneously.

---

## 🏢 Business Problem Statement

Management previously struggled with fragmented reporting across sales and HR departments:
* **Sales Disconnect:** Difficulty evaluating regional (District/Division) performance, daily/monthly revenue trends, and brand popularity side-by-side.
* **HR Visibility Gaps:** Inability to correlates employee turnover rates, work-life balance scores, and job satisfaction levels with organizational costs and longevity.
* **Strategic Blind Spots:** Lack of cross-departmental insights to ensure sales targets are adequately supported by a stable, satisfied workforce.

**Solution:** A 2-page interactive Power BI dashboard (**Beverage Sale & Performance Analytics** and **HR Analytics & Workforce Overview**) designed to drive data-informed strategic planning.

---

## 🛠️ Tools & Technologies

* **Business Intelligence:** Power BI Desktop
* **Data Transformation & ETL:** Power Query
* **Analytics & Calculations:** DAX (Data Analysis Expressions)
* **Data Architecture:** Star Schema / Data Modeling
* **Source Data Formats:** Microsoft Excel (`raw_data.xlsx`)

---

## 📊 Dashboard Overview & Key Insights

### Page 1: Beverage Sale & Performance Analytics

Focused on commercial revenue generation, volume, and geographic/brand distribution across Bangladesh districts and divisions.

![Beverage Sales Dashboard](docs/images/sales_analytics.png) *(Placeholder for screenshot)*

* **Key Performance Indicators (KPIs):**
  * **Total Revenue:** $8,201,115.00
  * **Average Price Per Unit:** $0.48
  * **Total Units Sold:** 16,450,500
* **Interactive Slicers:** District (e.g., Bagerhat, Chittagong), Beverage Brand, Division (e.g., Barishal, Chittagong, Dhaka, Khulna, Rajshahi).
* **Key Visual Insights:**
  * **Revenue Trend:** Revenue peaks significantly in Month 7 ($0.97M) and Month 12 ($0.98M).
  * **Brand Popularity (Revenue Share):**
    * **Coca-Cola:** 23.4% ($1.92M)
    * **Dasani Water:** 19.99% ($1.64M)
    * **Diet Coke:** 16.93% ($1.39M)
    * **Sprite:** 14.1% ($1.16M)
    * **Powerade:** 13.79% ($1.13M)
    * **Fanta:** 11.8% ($0.97M)
  * **Weekly Sales Pattern:** Units sold reach their peak towards the end of the week (Day 7 peaking at 2.63M units).
  * **Profit vs. Revenue Breakdown:** Dasani Water and Coca-Cola remain top drivers for both gross revenue and profit margins.

---

### Page 2: HR Analytics & Workforce Overview

Provides operational visibility into talent acquisition, retention risk, job satisfaction, and compensation distribution.

![HR Analytics Dashboard](docs/images/hr_analytics.png) *(Placeholder for screenshot)*

* **Key Performance Indicators (KPIs):**
  * **Total Workforce:** 1,470 employees
  * **Terminated Employees:** 237 employees
  * **Current Active Employees:** 1,233 employees
  * **Termination Rate:** 16.1%
  * **Total Salary Expense:** $9,559K ($9.56M)
* **Key Visual Insights:**
  * **Gender Distribution (Current Employees):** 59.37% Male (732) vs. 40.63% Female (501).
  * **Hiring Pace:** Consistent onboarding throughout the year (~347 to 382 new hires per quarter).
  * **Education Demographics:** Highest concentration of active employees hold a **Bachelor** degree (473), followed by **Master** degree holders (340).
  * **Work-Life Balance & Job Satisfaction:**
    * A majority of active employees report "Better" work-life balance (766 employees), while 55 report "Bad".
    * Over **62%** of active employees rate their job satisfaction as "High" (369) or "Very High" (407).
  * **Compensation vs. Tenure:** Salary expenditure scales with years at the company, with the largest concentration of salary expenditure centered around employees in their first 1–10 years of service.

---

## 🗂️ Data Architecture & Data Model

The project utilizes data imported and transformed via **Power Query**:
1. **Cleaning & Transformation:**
   * Handled missing values, formatted data types across age, attrition status, travel frequency, and departmental roles.
   * Standardized ratings (`EnvironmentSatisfaction`, `JobInvolvement`, `JobSatisfaction`, `WorkLifeBalance`) for categorical reporting.
2. **Key Entities:**
   * `Dataset` / `Data`: Primary HR employee table containing demographic, tenure, role, and satisfaction attributes.
   * `Dates`: DimDate table supporting time-intelligence functions for revenue and salary trend analysis.
   * `Cost` / `Sales`: Fact table detailing transactions, units sold, product pricing, and profit breakdowns.

---

## 💡 Strategic Recommendations

1. **Sales & Distribution Optimization:**
   * **Inventory Alignment:** Scale up distribution leading into peak sales periods (Months 7 & 12) to prevent stockouts of high-demand brands like Coca-Cola and Dasani Water.
   * **Weekend Supply Chain:** Leverage the peak in unit sales on Days 6 & 7 by ensuring weekend logistics and retail stocking are fully optimized.
2. **Workforce & Retention Strategies:**
   * **Targeted Turnover Mitigation:** Investigate root causes behind the **16.1% termination rate**, cross-referencing employees reporting low Work-Life Balance and low Job Satisfaction.
   * **Talent Development:** Focus retention programs on mid-tenure employees (1–5 years) where salary distribution and potential turnover risk intersect.

---

## 🚀 How to Open and View

### Prerequisites
* [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (October 2024 build or newer recommended).

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/beverage-sales-workforce-analytics.git
   ```
2. Open the file `Beverage_sales_and_workforce_analytics_dashboard.pbix` in Power BI Desktop.
3. If prompted to update data source paths, edit the data source setting in Power Query to point to `data/raw_data.xlsx`.

---

## 📁 Repository Structure

```text
├── data/
│   └── raw_data.xlsx          # Source Excel workbook
├── docs/
│   └── images/                # Screenshots for documentation
├── Beverage_sales_and_workforce_analytics_dashboard.pbix  # Main Power BI Report
└── README.md                  # Project Documentation
```