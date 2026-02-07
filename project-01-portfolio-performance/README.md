# Project Portfolio Performance Dashboard

**Goal:**  
Provide leadership with a clear, executive‑level view of project portfolio health by summarizing scope, financial exposure, and risk in a single, interactive dashboard.

This project demonstrates how portfolio data can be modeled and visualized to support decision‑making, prioritize risk, and enable stakeholder self‑service.

---

## What the Dashboard Shows

### Portfolio KPIs
- **Total Projects** – overall portfolio size  
- **Total Portfolio Budget** – total financial exposure  
- **At‑Risk Projects** – count of projects flagged as at risk  
- **% of Projects At Risk** – risk concentration across the portfolio  
- **Avg Budget per Project** – average investment per initiative  

### Visual Insights
- **Projects by Status** – distribution of portfolio health  
- **Budget by Project** – where financial exposure is concentrated  

### Interactivity
- **Project Manager slicer** to filter KPIs and visuals for stakeholder‑specific views

---

## Data & Model

- **Dataset:** Synthetic portfolio dataset (`projects.csv`) created for demonstration purposes  
- **Key Fields:**  
  - project_id  
  - project_name  
  - project_manager  
  - start_date  
  - end_date  
  - status  
  - budget  

- **Modeling Approach:**  
  - Clean, typed columns (dates and currency)  
  - Semantic model built in Power BI  
  - Reusable DAX measures for consistent portfolio metrics  

### Key DAX Measures
- `Total Projects`  
- `Total Budget`  
- `At Risk Projects`  
- `% At Risk`  
- `Avg Budget per Project`

---

## Tools Used
- **Power BI** (data modeling, DAX measures, dashboard design)  
- **DAX** (portfolio KPIs and calculations)  
- **Excel / CSV** (dataset creation and preparation)

---

## Dashboard Preview

### Portfolio Overview
![](./screenshots/pmo-portfolio-dashboard-full.png)

### KPI Summary
![](./screenshots/pmo-portfolio-dashboard-kpis.png)

---

## Key Takeaways
- Portfolio‑level KPIs provide immediate visibility into scope, spend, and risk  
- Risk concentration is highlighted without overwhelming the dashboard  
- Interactive filtering enables leaders to quickly explore ownership and impact  

---

## Potential Enhancements
- Add task‑level data to calculate **On‑Time %**  
- Add a risk register to analyze **risk severity and aging**  
- Add monthly financials to track **budget vs actual trends** over time
