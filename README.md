# Real-Time-Weather-ETL-Dashboard

It is an end-to-end real-time **ETL (Extract, Transform, Load)** pipeline project that collects **daily weather data** for **Sylhet, Bangladesh** using a public weather API. The data is processed using **Python**, stored in **Google BigQuery**, and visualized through **Metabase** in the form of a real-time dashboard.

This project showcases how to combine **data engineering**, **cloud storage**, and **data visualization** tools to turn raw API data into useful, real-time business insights.

---

## 🎯 Objective

The primary goal of this project is to create an **automated and scalable data pipeline** for fetching and visualizing **daily weather data**. The project uses the ETL architecture to:
- **Extract** daily weather data from a public API.
- **Transform** the raw data into a clean, structured format.
- **Load** the cleaned data into a BigQuery table.
- **Visualize** the real-time weather trends in a Metabase dashboard.
- **Automate** the entire process using a scheduler (Windows Task Scheduler).

---

## 🛠️ Technologies Used

| Tool/Technology | Purpose |
|------------------|---------|
| [Python](w) | Scripting language used for ETL logic |
| [Requests](w) | To call the weather API |
| [Pandas](w) | For transforming and cleaning JSON data |
| [Google BigQuery](w) | Cloud storage for weather data |
| [Google Cloud Client Library](w) | Python library to connect with BigQuery |
| [Metabase](w) | Business Intelligence tool for dashboard visualization |
| [Windows Task Scheduler](w) | Automation tool to run ETL script daily |

---


---

## 🧪 Project Workflow

### 🔹 1. Extract
- Use Python’s `requests` library to fetch **real-time weather data** for Sylhet via a public weather API (e.g., [OpenWeatherMap](w)).
- The data is received in **JSON** format.

### 🔹 2. Transform
- Use `pandas` to normalize the JSON structure.
- Drop irrelevant columns like visibility, timezones, etc.
- Add timestamps, format values, and ensure schema consistency.

### 🔹 3. Load
- Authenticate and connect to your **Google BigQuery** project using a service account.
- Create a table (if not already exists) in BigQuery.
- Append new weather data to the table on a daily basis.

### 🔹 4. Automate
- The Python script is set up to run **once every day** via **Windows Task Scheduler**.
- This ensures that daily weather data is always updated without manual effort.

### 🔹 5. Visualize
- Connect **BigQuery** as a data source to **Metabase**.
- Create an interactive **dashboard** showing:
  - Temperature trends
  - Humidity levels
  - Wind speed
  - Weather conditions (clouds, rain, etc.)
  - Date-wise breakdowns

---


