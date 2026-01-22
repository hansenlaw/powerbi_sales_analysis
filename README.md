# Sales Analysis Dashboard
### Power BI Portfolio Project

An interactive Sales Analysis Dashboard built with Power BI to provide comprehensive business performance insights.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

---

## Overview

This dashboard transforms raw sales data into actionable intelligence through advanced visualizations, dynamic filtering, and drill-through capabilities.

**Key Highlights:**
- 11-page interactive dashboard with intuitive navigation
- 91 visual components for comprehensive data storytelling
- 7 core KPIs tracking business performance
- Multi-dimensional analysis across Period, Country, Segment, and Product

---

## Screenshots

### Home Page
> Main landing page with navigation buttons
![alt text](<Screenshot 2026-01-22 223919.png>)

### Sales Analysis Dashboard
> Comprehensive overview with all KPIs and interactive charts
![alt text](<Screenshot 2026-01-22 224216.png>)

---

## Business Problem

| Challenge | Impact |
|-----------|--------|
| Scattered data sources | No single source of truth |
| Manual reporting | Time-consuming and error-prone |
| Limited visibility | Unable to track profit margins |
| No comparative analysis | Difficult to compare segments |
| Static reports | No drill-down capability |

---

## Solution

Built a centralized, interactive dashboard with:

1. **Star Schema Data Model** - Optimized query performance
2. **DAX Measures** - Dynamic calculations for accurate KPIs
3. **Interactive Design** - Cross-filtering and drill-through analysis
4. **Intuitive UX** - 30 action buttons for seamless navigation

---

## Dashboard Structure

| Page | Purpose |
|------|---------|
| Home | Landing page with navigation |
| Sales Analysis | Primary dashboard with KPIs |
| Help | User guide |
| Units Sold | Drill-through: quantity metrics |
| Net Sales | Drill-through: revenue breakdown |
| Net Profit | Drill-through: profitability |
| Cost of Goods | Drill-through: cost structure |
| Tooltips (4) | Custom hover information |

---

## Key DAX Measures

```dax
-- Core Metrics
M_Net Sales = SUM(FACT_SALES[Sales])
M_Profit = [M_Net Sales] - [M_Cost Of Goods]
M_Profit Margin = IFERROR([M_Profit] / [M_Net Sales], 0)

-- Year-over-Year Analysis
M_Profit YOY% = IFERROR(
    CALCULATE(([M_Profit CY] - [M_Profit PY]) / ABS([M_Profit PY]),
    ALL(DIM_DATE[Year])), 1
)
```

---

## Features

- **8 Filter Categories**: Year, Quarter, Period, Country, Segment, Product, Manager, Discount Band
- **Drill-Through Analysis**: Right-click on data points for detailed breakdowns
- **Custom Tooltips**: Hover for additional context
- **Sparkline Trends**: Mini-charts showing monthly trends

---

## Technical Skills

| Technical | Analytical |
|-----------|------------|
| Power BI Desktop | Business Requirements |
| DAX Development | KPI Definition |
| Star Schema Modeling | Data Storytelling |
| Advanced Visualizations | Dashboard UX Design |
| Drill-through & Tooltips | Multi-dimensional Analysis |

---

## Files

| File | Description |
|------|-------------|
| `Sales Analysis Report - blank.pbix` | Power BI dashboard file |

---

## How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Navigate using Home page buttons
4. Filter data using slicers on the right panel
5. Right-click for drill-through analysis
6. Hover over visuals for tooltips

---

## Author

**Hansen**

---

*Built with Power BI Desktop*
