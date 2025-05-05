
# Day 1 Journal - COVID-19 Data Engineering Project

## 📌 Objective
Build an end-to-end data engineering pipeline on COVID-19 data using Azure Data Lake, Databricks, Delta Lake, and Hive.

## 📂 Repository Structure (Initial)
```
/notebooks/
/data-samples/
  └── raw/
  └── cleaned/
/scripts/
/images/
/docs/
README.md
```

## 📥 Dataset Source
- Source: [Our World in Data - GitHub](https://github.com/owid/covid-19-data)
- File used: `owid-covid-data.csv`

## 🧾 Fields of Interest
- `location`
- `date`
- `total_cases`, `new_cases`, `total_deaths`
- `people_vaccinated`, `population`
- `tests_per_case`, `reproduction_rate`

## 🔍 Initial Observations
- Dataset includes global COVID-19 metrics updated daily.
- Missing values present in `people_vaccinated`, `reproduction_rate`.
- Some columns (like `iso_code`, `continent`) not needed for initial processing.

## 🧹 Cleaning Process (Sample Countries: India, USA)
- Dropped: `iso_code`, `continent`, `excess_mortality`
- Converted `date` to standard datetime format.
- Renamed columns for clarity.
- Filled missing numeric fields with 0 (temporary).

## ✅ Outputs
- Raw dataset saved in `/data-samples/raw/`
- Cleaned samples in `/data-samples/cleaned/`
- Initial EDA notebook in `/notebooks/day1_eda.ipynb`

## 📅 Next Steps
- Upload dataset to Azure Data Lake (ADLS Gen2)
- Set up bronze Delta table ingestion notebook on Databricks
- Start data profiling pipeline

---
