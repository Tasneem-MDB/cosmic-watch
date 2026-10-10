# Cosmic Watch: Explore Asteroids Near Earth

A pipeline that collects NASA NeoWs asteroid data daily, models it in PostgreSQL with dbt,
and shows close approaches and trends in a Streamlit dashboard.

## Stack
Python · PostgreSQL · dbt · Airflow · Docker · Streamlit

## Structure
| Folder | Purpose |
|---|---|
| `ingestion/` | Python scripts that call the NASA API; `raw_data/` holds the original JSON |
| `sql/` | Table definitions / schema |
| `dbt/` | Staging and analytical models + data-quality tests |
| `airflow/dags/` | Daily update DAG |
| `streamlit_app/` | Dashboard |
| `docker/` | Dockerfiles and compose config |
| `docs/` | Architecture diagram, notes |

## Getting started
1. `cp .env.example .env` and add your NASA API key (https://api.nasa.gov)
2. `python -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt`

## Workflow
- Branch from `main`: `cos-12-short-description` (use the Linear issue ID)
- Open a PR with `Closes COS-12` in the description; Linear moves the issue automatically
