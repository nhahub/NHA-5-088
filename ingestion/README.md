# Ingestion

Downloads the monthly BTS On-Time Performance files and stores them unchanged in the Bronze layer.

**Owner:** Asmaa Adel Ali (Data Ingestion Engineer)

---

## What goes here

* `download_bts.py` — downloads one month of BTS data with the 32 selected columns
* Airflow DAGs — monthly schedule, retries (3 times), failure alerts and the July–December 2025 backfill
* Lookup table downloads — BTS carrier and airport names, airport coordinates

## Output

Raw CSV files in the Bronze layer, one folder per month, with load time and file name (FR-01, FR-02).

## Azure equivalent

Azure Data Factory (copy activity and pipeline scheduling).
