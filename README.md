
# Delta Lake Project: COVID-19 Vaccination Data Pipeline

## 📊 Project Overview
This project demonstrates a complete Delta Lake pipeline using Databricks Unity Catalog with Bronze, Silver, and Gold tables for processing and analyzing global COVID-19 vaccination data.

## 🧱 Architecture

```
Raw (CSV Uploads) → Bronze (Ingestion) → Silver (Transformations & Cleaning) → Gold (Aggregations & Insights)
```

          +----------------+
           |  Raw CSV Files |
           +----------------+
                   |
                   v
           +----------------+
           |   Bronze Layer |
           | (Raw Ingested) |
           +----------------+
                   |
                   v
           +----------------+
           |   Silver Layer |
           | (Cleaned &     |
           |  Filtered)     |
           +----------------+
                   |
                   v
           +----------------+
           |    Gold Layer  |
           | (Aggregated &  |
           |  BI Ready)     |
           +----------------+
---

## 🗂️ Unity Catalog Structure

- **Catalog**: `databricks_cat`
- **Schemas**:
  - `raw`: CSV files
  - `bronze`: Ingested Delta tables
  - `silver`: Cleaned and transformed data
  - `gold`: Analytical gold tables

## 🏗️ Delta Lake Features Used

- **ACID transactions** with Delta Lake
- **Time travel** and versioning
- **Schema evolution** with evolving input data
- **Upserts/Merge** for incremental loads
- **Data cleanup** with `VACUUM`

---

## 🔍 Gold Layer Visualizations

1. **Total Vaccinations by Country (Latest Month)**  
2. **Vaccination Trends Over Time (Top 3 Countries)**  
3. **Vaccination by Manufacturer (via Joins)**  

*All plots are rendered using Python (matplotlib/seaborn) or can be connected via Power BI for dashboards.*

---

## 🔁 Delta Table Operations

- Schema enforcement
- Merge/Upsert logic
- Time-travel queries using `timestampAsOf` and `versionAsOf`

## 🧹 Maintenance

- Vacuum unused files with retention override
```python
spark.conf.set("spark.databricks.delta.retentionDurationCheck.enabled", "false")
deltaTable.vacuum(0)  # Run with caution
```

---

## 📈 Future Enhancements

- Power BI / Tableau integration with `gold` layer
- ML integration using `silver` or `gold` data
- Real-time streaming ingestion into `bronze`

---

## 🚀 Usage

Use this project to demonstrate:
- Your data engineering skills with Delta Lake
- Best practices with Databricks and Unity Catalog
- Real-world handling of public health datasets

---

## 🧠 Credits

Data Source: [Our World in Data - COVID-19 Vaccination](https://ourworldindata.org/covid-vaccinations)

---

## 📬 Contact

If you found this project helpful or want to collaborate, feel free to connect:

- 💼 LinkedIn: Ayub Khan https://www.linkedin.com/in/ayub-khan-85073556/
- 📧 Email: khanayubchand@gmail.com
