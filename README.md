# Retail Business Intelligence & Analytics Portfolio

A comprehensive 5-practical analytics project covering the full BI workflow — from SQL data extraction and diagnostic charting to geospatial Power BI dashboards, advanced AI-enabled visuals, and systematic academic research analysis.

**Domain:** National Retail Company (Multi-Region, Multi-Category)  
**Dataset:** 1,848 records · 2023–2024 · PKR 149M total sales · 5 regions · 6 provinces · 7 categories  
**Tools:** SQL · Python (Matplotlib, Pandas, NetworkX) · Power BI · Excel

---

## Project Structure

```
retail-bi-analytics/
├── dataset/
│   ├── RETAIL_TRANSACTIONS.csv        # Main flat table (1,848 rows)
│   └── Retail_Dataset_All_Practicals.xlsx  # Star schema (Fact + 3 Dimensions)
├── practical-1-sql-core-analytics/
│   └── Practical_1_Completed.docx
├── practical-2-diagnostic-charts/
│   └── Practical_2_Completed.docx
├── practical-3-geospatial-powerbi/
│   └── Practical_3_Completed.docx
├── practical-4-advanced-ai-visuals/
│   └── Practical_4_Completed.docx
└── practical-5-systematic-review/
    ├── Practical_5_Completed.docx
    └── P5_Papers_Dataset.xlsx
```

---

## Practicals Overview

### Practical 1 — SQL Core Analytics
**20 SQL queries** ranging from basic aggregations to advanced window functions, each paired with a chart.

| Concept | Techniques Used |
|---|---|
| Regional & category sales | `GROUP BY`, `ORDER BY`, `SUM` |
| Monthly trend analysis | `YEAR`, `MONTH` grouping, line/area charts |
| Stacked & clustered visuals | Multi-dimensional grouping |
| Rolling averages | `AVG() OVER (ROWS BETWEEN ...)` |
| MoM change analysis | `LAG()` window function |
| Regional dominance | `DENSE_RANK() OVER (PARTITION BY ...)` |
| Province-level filtering | `WHERE` clause, dual-axis charts |
| Growth % calculation | `NULLIF()`, percentage change formulas |

**Visualisations:** Bar, Column, Line, Area, Stacked Bar/Column, Clustered Bar/Column, Combo, Dual-Axis

---

### Practical 2 — Diagnostic Analytics Charts
**20 analytical questions** exploring *why* performance patterns occur, using advanced chart types.

| Analysis | Chart Type |
|---|---|
| Sales vs units efficiency | Scatter Chart |
| Regional & province outliers | Scatter / Bubble Chart |
| Category ranking shifts | Ribbon Chart (rank over time) |
| Sales build-up & drop-off | Waterfall Chart |
| Volume reduction stages | Funnel Chart |
| Efficiency vs growth trade-off | Quadrant Scatter |
| Market share gain/loss | Line Chart (time series) |
| Cross-region imbalance | Grouped Bar Chart |

**SQL techniques:** `RANK()`, `FIRST_VALUE()`, `STDDEV()`, `PCT_CHANGE`, `VARIANCE`

---

### Practical 3 — Geospatial & Multi-Dimensional Analytics (Power BI)
**20 Power BI visuals** built on a star schema using Time, Geography, and Category dimensions.

| Visual Category | Questions | Key Techniques |
|---|---|---|
| Map / Filled Map | Q1–Q5 | Geographic aggregation, YoY choropleth |
| Shape Map | Q6–Q8 | Category dominance, ASP classification |
| Azure Maps (heatmap) | Q9–Q10 | Monthly hotspots, volatility |
| Table / Matrix | Q11–Q14 | Cross-dimensional pivot |
| Card / Multi-row Card | Q15–Q18 | KPI summaries |
| KPI / Gauge | Q19–Q20 | MoM growth, benchmark comparison |

**SQL techniques:** Star schema joins, `PERCENTILE_CONT`, `QUALIFY RANK()`, `STDDEV()`, `CASE` classification

---

### Practical 4 — Advanced Analytics & AI-Enabled Visuals (Power BI)
**20 advanced Power BI visuals** including AI-powered components.

| Visual | Purpose | SQL Technique |
|---|---|---|
| Pie (Pareto) | Category contribution + cumulative % | `SUM() OVER (ORDER BY ... ROWS UNBOUNDED)` |
| Donut (Long Tail) | Province segmentation | `PERCENT_RANK()` |
| Treemap (HHI) | Market concentration index | Herfindahl-Hirschman Index formula |
| Treemap (YoY Growth) | Hierarchical growth comparison | Year-pivot with growth % |
| Slicer (NTILE Tiering) | Dynamic province filtering | `NTILE(3)` |
| Decomposition Tree | Growth driver drill-down | `LAG()` + multi-level hierarchy |
| Key Influencers | High-sales determinants | Mean + StdDev threshold classification |
| Q&A Visual | Natural language dataset | Semantic dataset with all metrics |
| KPI | Rolling 6-month momentum | `AVG() OVER (ROWS BETWEEN 5 PRECEDING ...)` |
| Gauge | Sales stability index | Inverse volatility index |

---

### Practical 5 — Systematic Literature Review: Agentic AI
A complete research data analysis on **Agentic AI (LLM-Based Autonomous Agents)** covering 18 papers (3 SLRs + 15 research papers, 2024–2025).

| Analysis | Method | Visualisation |
|---|---|---|
| Basic analysis | Frequency counts | Bar chart (domain distribution) |
| Publication trend | Year-wise count | Line chart |
| Dataset analysis | Type classification | Pie + Bar charts |
| Method analysis | Cross-tabulation | Stacked bar chart |
| Contribution analysis | Category grouping | Donut chart |
| Similarity analysis | Graph theory | Network graph (NetworkX) |
| Relationship analysis | Cross-dimensional matrix | Heatmap + Scatter |
| Research gap analysis | Coverage benchmarking | Gap bar chart |

**Key Finding:** Agentic AI dominates with 12/18 papers. Critical gaps identified in Cyber Security, Education AI, and Finance AI. Explainability and federated learning are entirely missing from the current literature.

---

## Dataset Schema

### Flat Table: `RETAIL_TRANSACTIONS`
| Column | Type | Description |
|---|---|---|
| `YEAR` | INTEGER | 2023 or 2024 |
| `MONTH_NUMBER` | INTEGER | 1–12 |
| `MONTH_NAME` | VARCHAR | January–December |
| `SEASON` | VARCHAR | Winter, Spring, Summer, Autumn |
| `REGION` | VARCHAR | North, South, East, West, Central |
| `STATE_PROVINCE` | VARCHAR | Punjab, Sindh, KPK, Balochistan, AJK, GB |
| `CATEGORY` | VARCHAR | Electronics, Clothing, Furniture, etc. |
| `SALES` | DECIMAL | Monthly sales in PKR |
| `UNITS` | INTEGER | Units sold |

### Star Schema (for Power BI Practicals 3 & 4)
- `FACT_SALES` — Transaction fact table with foreign keys
- `DIM_TIME` — 24 rows (Year × Month)
- `DIM_GEOGRAPHY` — 11 rows (Region × Province with lat/lon)
- `DIM_CATEGORY` — 7 rows (Category with average unit price)

---

## Skills Demonstrated

**SQL:** Window functions (`LAG`, `LEAD`, `RANK`, `DENSE_RANK`, `NTILE`, `PERCENT_RANK`), aggregations, CTEs, subqueries, star schema joins, HHI computation, rolling averages, YoY growth, NULLIF safety, CASE classification

**Python:** Matplotlib (10+ chart types), Pandas, NumPy, NetworkX (graph analysis), data generation and transformation pipelines

**Power BI:** Map, Filled Map, Shape Map, Azure Maps, Table, Matrix, Card, KPI, Gauge, Slicer, Treemap, Decomposition Tree, Key Influencers, Q&A Visual

**Analytics:** Descriptive, diagnostic, trend, geospatial, concentration (HHI), volatility, market share, systematic literature review methodology

---

## How to Use

1. Download the dataset from the `dataset/` folder
2. Open any `.docx` file to see the complete SQL query + result table + visualisation for each question
3. Import `Retail_Dataset_All_Practicals.xlsx` directly into Power BI using the sheet tabs as tables
4. For the star schema, connect tables on `TIME_KEY`, `GEO_KEY`, and `CAT_KEY`

---

*Built as part of a Business Intelligence & Data Analytics course, April 2026.*
