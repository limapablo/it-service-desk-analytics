# Project Architecture

```text
IFPA Open Data
      |
      v
Annual CSV Files (2020–2026)
      |
      v
Python Ingestion
      |
      +--> Schema profiling
      +--> Cleaning
      +--> Data-quality validation
      |
      v
Processed Analytical Dataset
      |
      v
PostgreSQL
      |
      +--> Analytical model
      +--> KPI views
      +--> Business analysis
      |
      v
Power BI
      |
      +--> Executive Overview
      +--> Operational Performance
      +--> Insights & Improvement Opportunities
```

## Design Principles

- Preserve raw source files unchanged.
- Separate exploratory work from reusable transformation code.
- Make cleaning and validation rules explicit and reproducible.
- Do not invent metrics that are unsupported by source fields.
- Treat 2026 as a partial year in year-over-year comparisons.
- Avoid exposing requester-level information in portfolio outputs.
