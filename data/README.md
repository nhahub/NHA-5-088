# Data

Local data folder. **Nothing in this folder is committed** except this file (see `.gitignore`).

The BTS files for July–December 2025 (3,554,943 flights, about 540 MB as CSV) are too large for Git. Each team member keeps them locally:

```text
data/
├── raw/      monthly BTS files (flights_2025_07.csv ... flights_2025_12.csv)
└── sample/   small extracts used by the tests
```

Source: [BTS Airline On-Time Performance](https://www.transtats.bts.gov/DL_SelectFields.aspx?gnoyr_VQ=FGJ), US government public data.
