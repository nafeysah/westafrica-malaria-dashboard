# Malaria Incidence in West Africa (2000–2024): A Power BI Analysis

## Overview
This project analyzes malaria incidence trends across 12 West African countries from 2000 to 2024, using data sourced from the World Health Organization's Global Health Observatory (via Our World in Data). The goal is to identify which countries have made the most progress against malaria over the past two decades, and to surface patterns worth further investigation.

## Business/Research Question
How has malaria incidence changed across West African countries between 2000 and 2024, and which countries have improved most relative to their neighbors?

## Data Source
- **World Health Organization, Global Health Observatory** — malaria incidence data (new cases per 1,000 population at risk), processed and redistributed by Our World in Data
- **Scope:** 12 West African countries — Benin, Burkina Faso, Côte d'Ivoire, Ghana, Guinea, Liberia, Mali, Niger, Nigeria, Senegal, Sierra Leone, Togo
- **Time range:** 2000–2024

## Tools Used
- **Power Query** — data import and filtering to the West Africa country set
- **Power BI Data Model** — single flat table, no additional relationships required
- **DAX** — custom measures for year-specific and percent-change calculations
- **Power BI Desktop** — visuals and dashboard assembly

## DAX Measures
- `Incidence 2000` — average incidence in the baseline year, via `CALCULATE`
- `Incidence 2024` — average incidence in the latest year, via `CALCULATE`
- `Pct Change 2000-2024` — percent change between the two, via `DIVIDE`

## Dashboard Components
1. **Bar chart** — average incidence per country (2000–2024), ranking countries from highest to lowest burden
2. **Line chart** — incidence trend over time, all 12 countries plotted together
3. **% Change table** — percent change in incidence from 2000 to 2024, per country
4. **Filled map** — West Africa, all 12 countries labeled for geographic context

## Key Findings
- **Senegal shows the most dramatic improvement in the region**, with malaria incidence falling by approximately **84% between 2000 and 2024** — far outpacing every other country in the dataset. This consistent, steady decline is visible throughout the entire study period, not just in recent years.
- **Burkina Faso carries the highest average incidence** in the region across the full period, consistently at the top of the bar chart ranking.
- Most countries in the region show a **general downward trend after roughly 2013–2015**, though the pace and consistency of improvement varies widely by country — several (e.g., Mali, Niger) show only modest overall change compared to Senegal's sharp decline.
- The scale of Senegal's outperformance raises a natural follow-up question: **what intervention or policy factors differ in Senegal** compared to its neighbors? This is a strong candidate for a follow-up analysis incorporating WHO intervention-coverage data (e.g., insecticide-treated net distribution).

## Files in This Repository
- `malaria_westafrica_dashboard.pbix` — full Power BI file
- `malaria_westafrica_dashboard.pdf` — static export of the dashboard
- `incidence-of-malaria.csv` — source data (West Africa subset)

## Possible Next Steps
- Incorporate WHO intervention-coverage data (bed net distribution, treatment access) to test whether Senegal's improvement correlates with specific interventions
- Extend the analysis to malaria mortality rates, not just incidence
- Build a companion SQL analysis answering the same core questions directly against the raw data

---
*Part of a self-directed data analytics portfolio, built alongside SQL and Excel projects covering sales and customer analytics.*
