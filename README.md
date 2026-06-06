# Report-Automation-Pipeline

# 📊 3M Automation Report Pipeline

An automated data pipeline designed to extract retail analytics from an enterprise data lake, map complex business dimensions, and compile multi-layered performance dashboards. It builds and deploys two distinct operational datasets—**Market Share (MS)** and **Share of Voice (SOV)**—directly to live reporting suites.

## 🚀 Pipeline Flow Architecture
[Trino Data Lake] ────> [SQL Query Extraction] ────> [Pandas Transformation Engine]
│
[Google Sheets API] <─── [Automated Sheet Deploy] <─── [Multi-Dimensional Mapping]

### 🔹 Stage 1: Extraction & Ingestion
* **Big Data Querying:** Connects to a Trino-backed enterprise data lake using distributed computing architecture.
* **Granular Extraction:** Runs optimized relational queries targeting historical regional SKU availability, revenue metrics, and organic/sponsored organic keyword impressions.

### 🔹 Stage 2: Dimension Mapping & Transformation
* **Dynamic Header Resolution:** Employs a case-insensitive matching fallback mechanism (`find_col`) to read and parse structural structural changes in mapping catalogs safely.
* **Layered Aggregations:** * Blends database brand variants into standardized operational reporting brands.
  * Resolves granular regional coordinates (`store_id`, `pincode`, `city_name`) into standardized territorial zones.
  * Re-allocates category structures based on an isolated SKU mapping schema.

### 🔹 Stage 3: Feature Engineering & Tabular Layouts
* **Derived Metrics Engine:** Calculates localized metrics, raw coverage ratios, and month-over-month string structures on the fly.
* **Side-by-Side Horizontal Pivoting:** Combines 5 distinct categorical aggregation structures side-by-side into a single matrix. Includes structural safety padding to prevent mismatched rows across uneven matrix lengths.

### 🔹 Stage 4: Automated Deployments
* **Remote Updates:** Connects securely to the Google Workspace engine via OAuth2 JSON key management.
* **High-Throughput Rendering:** Clears targets dynamically and dumps structural dataframes natively into structural reports (`MS_Basedata`, `MS_Pivot`, `SOV_Basedata`) using `gspread-dataframe`.
