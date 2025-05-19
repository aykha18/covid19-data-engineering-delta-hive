
# 📘 COVID-19 Vaccination Data Engineering Project – Comprehension Journal

**🗓️ Project Duration:** May 2025  
**👤 Author:** [Your Name]  
**📌 Dataset:** OWID COVID-19 Vaccination Data

---

## 1. Objective
The project aimed to implement a medallion architecture using **Azure Databricks**, **Delta Lake**, and **Unity Catalog** for COVID-19 vaccination data. The pipeline includes Bronze (raw), Silver (cleaned), and Gold (aggregated) tables, topped off with visual analytics.

---

## 2. Tools & Services Used
- Azure Data Lake Gen2
- Azure Databricks
- Unity Catalog (for governance)
- Delta Lake
- PySpark
- Power BI (planned for external consumption)
- GitHub (data source)

---

## 3. Learning Highlights

### ✅ Day 1: Project Setup
- **What worked:** Manual creation of Unity Catalog metastore from Azure UI.
- **Challenge:** Automating ingestion from GitHub failed due to malformed CSV.
- **Resolution:** Switched to manual upload to raw container.

### ✅ Day 2: Bronze Layer
- **Learned:** Read CSV from ADLS Gen2 and write as Delta to Unity Catalog.
- **Fix:** Used correct header option and ensured schema correctness.

### ✅ Day 3: Silver Layer
- **Focus:** Cleaned data, resolved date format issues (used `yyyy-MM-dd`).
- **Learned:** How to use `to_date()` and write transformed data to silver.

### ✅ Day 4: Gold Layer + Visualizations
- **Built:** Aggregated stats by country and manufacturer.
- **Used:** `groupBy()`, `agg()`, and filters to generate visual-ready tables.

### ✅ Day 5: Joins & Schema Evolution
- **Joined:** Manufacturer and total vaccinations tables.
- **Tested:** Schema evolution via `mergeSchema` and `.overwrite()` mode.

### ✅ Day 6: Time Travel & Versioning
- **Explored:** `timestampAsOf`, `versionAsOf` with Unity Catalog.
- **Reverted:** Used `.write().overwrite()` to roll back to older version.

### ✅ Day 7: Documentation
- **Finalized:** README.md, architecture diagram, and visual overview.
- **Learned:** Importance of governance, lineage, and cataloging.

---

## 4. Challenges Faced
- Data formatting issues from GitHub (extra HTML in CSV).
- Difficulty switching schemas within Unity Catalog in UI.
- Understanding Unity Catalog table paths vs volume paths.

---

## 5. Final Output
- ✅ Bronze: `databricks_cat.bronze.vaccinations_by_manufacturer`
- ✅ Silver: `databricks_cat.silver.vaccinations_by_manufacturer`
- ✅ Gold: `databricks_cat.gold.vaccinations_summary`

---

## 6. Future Work
- Automate ingestion with Azure Data Factory or Databricks workflows.
- Visualize with Power BI using direct lakehouse connection.
- Add testing and CI/CD for notebooks.
