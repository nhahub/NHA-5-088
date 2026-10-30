# Tests

Automated tests for every part of the pipeline, run by GitHub Actions on every pull request.

**Owner:** all team members (each member tests their own part)

---

## What goes here

* `pytest` unit tests that run on a small data sample (never the full files)
* One test file per part, for example `test_ingestion.py`, `test_silver.py`, `test_warehouse.py`

## Run

`pytest tests/`
