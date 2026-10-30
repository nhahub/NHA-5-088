# FlightLens: US Flight Performance Data Platform

An end-to-end data pipeline that turns raw US flight records from the Bureau of Transportation Statistics (BTS) into clean, tested, analysis-ready data, so airline and airport managers can see where, when and why flights are delayed or cancelled.

Capstone project for the **Digital Egypt Pioneers Initiative (DEPI), Round 5**, track **AI & Data Science – Microsoft Data Engineer**.

---

## Project Information

| Item | Details |
|---|---|
| Training provider | Skills Dynamix |
| Group | Group 3 · ALX5_AIS5_S6 |
| Instructor | Ahmed Essam Azab |
| Team | Nepal Adel Ali, Asmaa Adel Ali, Omar Emad Hamdy, Abdelrahman Mahmoud Mohamed, Mosaab Mohamed Mohamed |

---

## Project Documents

| Phase | Document |
|---|---|
| 1. Project Planning & Management | [FlightLens_Project_Proposal.pdf](docs/01_project_planning/FlightLens_Project_Proposal.pdf) |
| 2. Literature Review | [FlightLens_Literature_Review.pdf](docs/02_literature_review/FlightLens_Literature_Review.pdf) |
| 3. Requirements Gathering | [FlightLens_Requirements_Specification.pdf](docs/03_requirements/FlightLens_Requirements_Specification.pdf) |

---

## Data

* **Source:** BTS Airline On-Time Performance database, US Department of Transportation
* **Coverage:** US domestic flights, July to December 2025
* **Volume:** 3,554,943 flights
* **Licence:** US government public data, free to use

---

## Architecture

* **Ingestion:** Python and Apache Airflow
* **Processing:** PySpark and Delta Lake, through Bronze, Silver and Gold layers
* **Warehouse:** PostgreSQL star schema
* **Consumers:** Power BI dashboard, delay-prediction model (LightGBM, FastAPI), GenAI question-answering assistant
* **Deployment:** Docker Compose and GitHub Actions

---

## Repository Structure

| Folder | Content | Owner |
|---|---|---|
| [`ingestion/`](ingestion/) | BTS download, Airflow DAGs, Bronze layer | Asmaa Adel Ali |
| [`spark/`](spark/) | PySpark cleaning, Silver layer, data-quality checks | Mosaab Mohamed Mohamed |
| [`warehouse/`](warehouse/) | Star schema, Gold layer, PostgreSQL views | Nepal Adel Ali |
| [`dashboard/`](dashboard/) | Power BI report | Nepal Adel Ali |
| [`ml/`](ml/) | Delay-prediction model and API | Omar Emad Hamdy |
| [`assistant/`](assistant/) | GenAI question-answering assistant | Abdelrahman Mahmoud Mohamed |
| [`tests/`](tests/) | Automated tests | All members |
| [`docs/`](docs/) | Project documents for each DEPI phase | All members |
| [`data/`](data/) | Local data folder, not committed | — |

---

## Contributing

Every change goes through a branch and a pull request reviewed by another team member. Branch names, commit messages and pull-request rules are in [CONTRIBUTING.md](CONTRIBUTING.md).
