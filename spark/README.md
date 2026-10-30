# Spark (Silver Layer)

Cleans and standardizes the Bronze data with PySpark and Delta Lake, and runs the data-quality checks before data moves to Gold.

**Owner:** Mosaab Mohamed Mohamed (Big Data Engineer)

---

## What goes here

* PySpark jobs that clean and type the records: `hhmm` times to timestamps (2400 = 00:00 next day), next-day arrivals, nulls, flags, lookups
* Great Expectations checks: schema and types, one row per flight, valid codes and times
* Quarantine handling for rows that fail a critical check

## Output

Delta tables in the Silver layer, partitioned by year and month (FR-03, FR-04).

## Azure equivalent

Azure Databricks.
