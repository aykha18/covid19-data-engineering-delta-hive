
# COVID-19 Data Engineering Project

This project is an end-to-end data engineering pipeline built using **Azure Data Lake**, **Apache Spark (Databricks)**, **Delta Lake**, and **Apache Hive**, focusing on global COVID-19 data. It demonstrates how to ingest, clean, transform, and query data efficiently at scale.

## 🚀 Project Goals

- Ingest COVID-19 data from [Our World in Data](https://github.com/owid/covid-19-data)
- Store data in a multi-layer Delta Lake architecture: Bronze → Silver → Gold
- Transform and analyze the data using PySpark on Azure Databricks
- Query data using Apache Hive tables on Delta format
- Document and visualize results using notebooks and Power BI

## 🗂️ Project Structure

```
📁 covid19-data-engineering-delta-hive/
├── notebooks/           # Databricks notebooks (ETL, exploration, visualizations)
├── data-samples/        # Raw and cleaned sample data
│   ├── raw/
│   └── cleaned/
├── scripts/             # Helper PySpark scripts and jobs
├── images/              # Diagrams and architecture screenshots
├── docs/                # Project journal and documentation
├── README.md
```

## 🛠️ Technologies Used

- Azure Data Lake Storage (ADLS Gen2)
- Azure Databricks (PySpark, Delta Lake)
- Apache Hive
- Power BI or Databricks Notebooks for Visualization
- Git/GitHub for version control

## 📊 Dataset Source

- COVID-19 Dataset from [Our World in Data](https://github.com/owid/covid-19-data)
- File: `owid-covid-data.csv` (contains global cases, testing, deaths, vaccination metrics)

## 📅 Project Plan (10-Day Sprint)

| Day | Task |
|-----|------|
| 1   | Project setup + dataset exploration |
| 2   | Azure environment setup (Storage, Databricks) |
| 3   | Bronze layer ingestion |
| 4   | Silver layer transformation |
| 5   | Gold layer aggregation |
| 6   | Hive table creation and querying |
| 7   | Delta Lake features (time travel, schema evolution) |
| 8   | Visualization & dashboard |
| 9   | Final documentation |
| 10  | Testing, optimization, GitHub publishing |

## ✅ Outcomes

- End-to-end data pipeline on Azure with open lakehouse architecture
- Cleaned and versioned COVID-19 dataset stored as Delta tables
- Hive-accessible analytics-ready tables
- GitHub-hosted public portfolio project

## 📜 License

This project is open-source and available under the MIT License.
