# Financial Variance & Trend Analysis Dashboard

**Goal:**  Provide leadership with a clear view of **budget vs actual performance over time**, including **variance dollars**, **variance percentage**, and **department-level filtering** to quickly identify where over/underspend is occurring.

This project demonstrates time-aware financial analysis with reusable measures, executive-ready visuals, and stakeholder-friendly interactivity.

---

## What the Dashboard Shows

### Finance KPIs
- **Total Budget** – total planned spend over the selected period  
- **Total Actual** – total actual spend over the selected period  
- **Variance ($)** – dollar difference between actual and budget  
- **Variance (%)** – size of the miss as a percentage of budget  

### Visual Insights
- **Budget vs Actual (Monthly)** – side-by-side trend of planned vs actual spend  
- **Monthly Variance ($)** – over/under budget trend with a zero baseline for quick interpretation  

### Interactivity
- **Department slicer** to isolate where variance is concentrated (e.g., IT, HR, Operations)

---

## Data & Model

- **Dataset:** Synthetic monthly financials (`finance_monthly.csv`) created for demonstration purposes  
- **Key Fields:**  
  - `month` (YYYY-MM)  
  - `department`  
  - `budget` (planned)  
  - `actual` (actual spend)  

- **Modeling Approach:**  
  - Clean column typing (Date, Text, Whole Number)  
  - Reusable **DAX** measures for consistent financial logic  
  - Date axis configured as **continuous** (no hierarchy) for true trendlines

### Key DAX Measures
- `Total Budget = SUM(finance_monthly[budget])`  
- `Total Actual = SUM(finance_monthly[actual])`  
- `Variance ($) = [Total Actual] - [Total Budget]`  
- `Variance (%) = DIVIDE([Variance ($)], [Total Budget])`

*(All currency measures formatted as Currency with 0 decimals; Variance (%) formatted as Percentage.)*

---

## Tools Used
- **Power BI** (data modeling, DAX measures, time-series visuals, slicers)  
- **DAX** (financial KPIs and variance logic)  
- **Excel / CSV** (dataset creation and preparation)

---

## Dashboard Preview

### Financial Performance Overview
![Financial Variance Dashboard](./screenshots/finance-variance-dashboard-full.png)

### KPI Summary
![KPI Summary](./screenshots/finance-variance-dashboard-kpis.png)

---

## Key Takeaways
- Variance is tracked both in **absolute dollars** and **relative percentage**, giving leaders clarity on **materiality**  
- Trend lines make it easy to see **when** performance diverged from plan and whether it’s improving or worsening  
- Department filtering enables quick **drill-in** to the drivers of variance

---

## Potential Enhancements
- Add **YTD** and **MTD** variants of KPIs using time intelligence  
- Add **department ranking** by variance % (top/bottom performers)  
- Include **forecast** (e.g., trailing 3‑month average for next month’s actuals)  
- Add **tooltips** with mini-trends or sparklines for each department  
- Introduce **Budget vs Actual clustered columns** for an executive “at-a-glance” comparison by month


