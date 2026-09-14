# IT Service Desk Operational Analytics

End-to-end analytics project designed to evaluate service desk efficiency, workload distribution, operational bottlenecks, and service performance using public IT service desk data from the Instituto Federal do Pará (IFPA).

## Project Goal

The objective is to build a reproducible analytics workflow that transforms raw service desk records into reliable business insights.

The project is organized into three main analytical layers:

1. **Python** — ingestion, cleaning, validation, exploratory analysis, and data preparation.
2. **SQL / PostgreSQL** — analytical modeling, KPI calculation, reusable views, and business analysis.
3. **Power BI** — executive and operational dashboards for decision support.

## Business Questions

The project aims to answer questions such as:

- How has ticket volume evolved over time?
- Which categories concentrate the highest workload?
- Which categories present the longest resolution times?
- Is there seasonality by month, weekday, or time period?
- How does backlog evolve over time?
- Which operational areas should be prioritized for improvement?
- Which factors are associated with slower ticket resolution?

Additional SLA-related metrics will only be included if supported by the available source data.

## Data Source

The dataset contains public IT Service Desk tickets from IFPA and is provided as annual CSV files.

The official data dictionary documents the following core fields:

- Ticket ID
- Category
- Title
- Requester
- Opened date
- Closed date

The raw files cover 2020 through 2026, with 2026 being a partial year.

## Planned Architecture

```text
IFPA Open Data
      |
      v
 Annual CSV Files
      |
      v
    Python
  ingestion
  cleaning
  validation
      |
      v
  PostgreSQL
      |
      v
Dimensional / Analytical Model
      |
      v
   Power BI
      |
      v
Executive + Operational Dashboard
```

## Repository Structure

```text
it-service-desk-analytics/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
├── sql/
├── powerbi/
├── docs/
├── tests/
├── .gitignore
├── requirements.txt
└── README.md
```

## Project Roadmap

### Phase 1 — Data Understanding
- Inspect annual schemas
- Identify format changes across years
- Profile nulls, duplicates, and data types
- Document inconsistencies before consolidation

### Phase 2 — Data Ingestion & Cleaning
- Standardize column names and types
- Parse date fields
- Consolidate annual files
- Validate ticket identifiers and records
- Produce a clean analytical dataset

### Phase 3 — SQL Analytics
- Load processed data into PostgreSQL
- Build analytical views
- Calculate operational KPIs
- Apply CTEs, window functions, ranking, and time-series comparisons

### Phase 4 — Power BI
- Build a clean analytical model
- Create executive overview
- Create operational performance views
- Present actionable findings and recommendations

### Phase 5 — Documentation & Portfolio Polish
- Finalize architecture documentation
- Add dashboard screenshots
- Document key findings and limitations
- Make the project fully reproducible

## Tech Stack

- Python
- Pandas
- Jupyter
- PostgreSQL
- SQL
- Power BI
- Git / GitHub

## Status

**In progress — Phase 1: Data Understanding**

## Author

**Pablo Lima**

Data & Analytics | IT Governance | Process Excellence
