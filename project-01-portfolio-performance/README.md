# Project Portfolio Performance Dashboard

**Goal:** Give leadership a concise view of portfolio health—scope, financial exposure, and risk—using an executive-ready Power BI dashboard.

## What the dashboard shows
- **Total Projects** – portfolio scope
- **Total Portfolio Budget** – overall financial exposure
- **% of Projects At Risk** – concentration of risk
- **At‑Risk Projects** – count needing attention
- **Avg Budget per Project** – cost profile
- **Projects by Status** – distribution of portfolio health
- **Budget by Project** – where spend is concentrated
- **Slicer (Project Manager)** – quick stakeholder filtering

## Data & Model
- **Dataset:** `projects.csv` (project_id, project_name, project_manager, start_date, end_date, status, budget)
- **Modeling:** Typed columns (dates/currency), semantic model, DAX measures
- **Key measures (DAX):**
  - `Total Projects = DISTINCTCOUNT('projects 1'[project_id])`
  - `Total Budget = SUM('projects 1'[budget])`
  - `At Risk Projects = CALCULATE(DISTINCTCOUNT('projects 1'[project_id]), 'projects 1'[status] = "At Risk")`
  - `% At Risk = DIVIDE([At Risk Projects], [Total Projects])`
  - `Avg Budget per Project = DIVIDE([Total Budget], [Total Projects])`

## Next enhancements
- Add **tasks** data → On‑Time % KPI
- Add **risk** data → severity mix, aging
- Add **monthly financials** → budget vs actual, variance %
- Add a **timeline** view (start/end dates)





## Dashboard Preview

### Portfolio Overview
![](./screenshots/pmo-portfolio-dashboard-full.png)

### Key Visuals (Detail Views)
![](./screenshots/pmo-portfolio-dashboard-kpis.png)
