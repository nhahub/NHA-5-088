# Warehouse (Gold Layer)

Builds the Gold star schema from the Silver data and serves it from PostgreSQL to the dashboard, the ML model and the GenAI assistant.

**Owner:** Nepal Adel Ali (Analytics Engineer)

---

## What goes here

* SQL scripts: schema, keys, indexes and monthly partitions
* Dimension and fact loads: `fact_flights`, `dim_date`, `dim_time`, `dim_carrier`, `dim_airport`, `dim_route`
* The daily aggregate `agg_daily_airport_kpis`
* Read-only views and the read-only database role

## Output

The star schema in PostgreSQL with read-only views (FR-05, FR-07).

## Azure equivalent

Azure Synapse Analytics.
