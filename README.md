# HR Analytics — Databricks & Power BI

Data Engineering and Data Science project applied to real HR data (Business Case).

## Tools used

| Component | Technology |
|---|---|
| Compute | Databricks (Free edition) |
| Raw Storage | Unity Catalog Volume |
| Processed Storage | Delta Lake |
| Language | PySpark |
| Visualization | Power BI Desktop |
| Version Control | GitHub |

## Dataset

6 CSV files from a Belgian HR software system:

- `ABSENCES_fixed.csv` — 100,815 rows — monthly absences per employee
- `CONTRACT_BASIS_fixed.csv` — 29,452 rows — contract details
- `SALARY_STATEMENT_fixed.csv` — 267,166 rows — gross/net salaries
- `WORK_PLAN_fixed.csv` — 52,854 rows — work schedules and NACE codes
- `POSTCODES_fixed.csv` — 1,146 rows — postal codes → Belgian regions
- `Absence_Type_fixed.csv` — 8 rows — absence type reference table

## Project Structure

```
HR-analytics-databricks_PowerBI/
├── 01_ingestion_cleaning.ipynb   # CSV loading → Delta Lake
├── 02_transformation.ipynb       # Star schema, KPIs, FDCP key
├── 03_ml.ipynb                   # Clustering & anomaly detection
└── README.md
```

## Pipeline

```
Unity Catalog Volume (CSV)
        ↓
  Notebook 1 — Ingestion & Cleaning
        ↓
  Delta Lake (6 tables)
        ↓
  Notebook 2 — Transformations & Star Schema
        ↓
  Notebook 3 — ML (clustering, anomaly detection)
        ↓
  Power BI Dashboard
```

## Author

Michael Kahla — [www.linkedin.com/in/michael-kahla-74a0331b8](#) · [https://github.com/michael-kahla](#)
