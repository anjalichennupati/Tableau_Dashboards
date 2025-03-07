# Tableau Dashboards

This repository showcases three dashboards ranging from basic to advanced analytics, along with the datasets used for each. It includes insights on **data visualization, ETL processes, and interactive reporting** using Tableau Public.

## 📊 Dashboards Included

1. **Basic Airbnb Sales Dashboard** – A beginner-friendly dashboard displaying fundamental sales metrics.
<p align="center">
  <img src="https://i.postimg.cc/zBHwtXWD/Whats-App-Image-2025-03-06-at-23-15-29-dae2f935.jpg" alt="App Screenshot" width="600">
</p>  

2. **Sales Analytics Dashboard (Interactive)** An advanced dashboard incorporating interactive filters and deeper insights into sales performance.
<p align="center">
  <img src="https://i.postimg.cc/d31hH5g2/Whats-App-Image-2025-03-06-at-23-13-35-e0ef7393.jpg" alt="App Screenshot" width="600">
</p> 

3. **British Airways Dashboard (Interactive)** – A comprehensive dashboard utilizing geospatial data for airline reviews and analytics.
<p align="center">
  <img src="https://i.postimg.cc/85h88DgD/Whats-App-Image-2025-03-07-at-09-51-35-d327524f.jpg" alt="App Screenshot" width="600">
</p> 

🔗 **View My Tableau Public Profile**: [https://public.tableau.com/app/profile/anjali.chennupati/vizzes](#)

---




## 📌 Key Concepts in Tableau

### 🎯 Dimensions & Measures
- **Dimensions** – Qualitative (categorical) data (e.g., Customer Name, Product Category).
- **Measures** – Quantitative (numerical) data (e.g., Sales Amount, Profit).

### 🔄 Data Processing & ETL
- Data analytics follows the **AIMS GRID** framework: **Purpose, Stakeholders, End Result, Success Criteria**.
- **ETL (Extract, Transform, Load)** process is crucial for preparing data before visualization.
- Direct MySQL queries in Tableau slow down performance, so data transformation is preferred.

### 🔹 OLTP vs. OLAP
- **OLTP (Online Transaction Processing)** – Handles real-time transactions (e.g., banking, e-commerce orders).
- **OLAP (Online Analytical Processing)** – Used for deep historical analysis and data warehousing.

### 🛠 Data Cleaning in Tableau
- Since **Tableau Public** doesn’t support direct MySQL connections, all databases must be **exported as CSV**.
- Data modeling follows a **Star Schema**:
  - **Fact Table** (e.g., Transactions) at the center.
  - **Dimension Tables** (e.g., Products, Customers, Time) surrounding it.
- **Fixing Data Issues**: Use **Calculated Fields** to adjust inconsistencies (e.g., currency conversions).
  ```
  IF [Currency] = 'USD' THEN [Sales Amount] * 87 ELSE [Sales Amount] END
  ```

### 📅 Dynamic Filters for Dashboards
- Use **Year/Month as a column** and create a **Blank Calculated Field** in rows.
- Apply **global filters** in the dashboard under **floating layout** for seamless interaction.
- When all charts share the same column name, they **auto-update dynamically** when filtering.

### 🗺 Geospatial Analytics (British Airways Dashboard)
- To generate a **map visualization**, the metric must be set as **Global** to automatically derive **Longitude & Latitude**.
- Use **Parameter Controls** to enable user-defined interactive filters.
  ```
  IF [Metric] THEN [Show Metric Values] END
  ```
- This approach can be replicated across multiple map-based visualizations.

---

## 📂 Repository Structure
```
📂 Tableau Dashboards
│-- 📄 README.md
│   │-- Airbnb_Sales.twbx
│   │-- Sales_Analytics_Interactive.twbx
│   │-- British_Airways_Interactive.twbx
│-- 📁 Datasets

```

---

## 🚀 Getting Started
1. Download the `.twbx` files from this repository.
2. Open **Tableau Public**.
3. Import the dashboards and explore the visualizations!



