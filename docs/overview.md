# Project Pipeline Overview

This document captures the end‑to‑end concept for structuring iRNA/iRznA data, processing it, and making it available for analysis and interfaces.

## 1. Define Schema
**Core iRNA fields**
- Insight
- Resilience
- Navigation
- Agency

**Extended iRznA fields**
- Context
- Modulation
- Signal type

**Event metadata**
- Timestamp
- Trigger
- Environment

## 2. Repository Structure
```
/schema/       -> CSV, JSON, YAML definitions
/examples/     -> sample annotated events
/pipeline/     -> Python or Node scripts
/docs/         -> explanation for experts
```

## 3. Ingest Human Events
- CSV logs
- Form submissions
- Annotated episodes
- Optional sensor/behavioral data

## 4. Pipeline Stages
1. **Validation** — schema conformity checks
2. **Normalization** — labels, units, categories
3. **Enrichment** — derived metrics, iRNA/iRznA scores
4. **Versioning** — Git commits, tags

## 5. Cleaned Dataset Outputs
- Flat CSV
- Parquet (optional)
- SQLite/DuckDB (lightweight warehouse)

## 6. Analysis Layer
- Python notebooks (pandas, sklearn)
- R scripts (tidyverse)
- Optional ML models (clustering, pattern detection)

## 7. Data Warehouse
- SQLite or DuckDB file
- Queryable locally or via API

## 8. Interfaces
- Downloads (CSV, SQLite)
- API (FastAPI or Node)
- Dashboard (Streamlit, Dash, or simple HTML)