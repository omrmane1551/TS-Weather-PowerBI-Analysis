# 🌦️ TS Weather Data Analysis (2021–2024) | Power BI

## 📌 Project Overview
This project analyzes **Telangana weather data from 2021 to 2024** to identify **temperature trends, rainfall patterns, seasonality, and extreme weather events**.  
The dashboard is built using **Power BI**, following industry best practices such as **data modeling, DAX time intelligence, custom tooltips, and interactive visuals**.

---

## 📊 Power BI Dashboard File
Due to GitHub file size limits, the Power BI (`.pbix`) file is available in the **Releases** section of this repository.

👉 **Go to:** `Releases → v1.0 → Download TS_Weather_Analysis.pbix`

---

## 🎯 Project Objectives
- Analyze **average, maximum, and minimum temperature trends**
- Study **monthly and seasonal rainfall patterns**
- Perform **Year-over-Year (YoY)** and **Month-over-Month (MoM)** analysis
- Identify **extreme weather events** (heatwaves and heavy rainfall)
- Build a **professional, interactive Power BI dashboard**

---

## 🗂️ Dataset Information
- **Source:** Monthly CSV files (2021–2024)
- **Format:** CSV
- **Granularity:** Daily / Monthly weather records
- **Key Columns:**
  - Date
  - Avg / Max / Min Temperature
  - Rainfall
  - Year
  - Month Name
  - Month Number

---

## 🛠️ Tools & Technologies
- **Power BI Desktop**
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and time intelligence
- **CSV Files** – Raw data source

---

## 🧹 Data Preparation (Power Query)
- Combined all CSV files using **Folder Connector**
- Standardized column names and data types
- Removed null and invalid values
- Extracted **Year, Month Name, and Month Number**
- Created a clean **Weather_Fact** table

---

## 🧱 Data Modeling
- Implemented a **Star Schema**
- Created a dedicated **Date Table**
- Established relationship:

- Marked Date Table to enable accurate time intelligence

---

## 📐 Key DAX Measures
```DAX
Avg Temperature = AVERAGE ( Weather_Fact[Avg Temperature] )

Total Rainfall = SUM ( Weather_Fact[Rainfall] )

Rainfall LY =
CALCULATE (
  [Total Rainfall],
  SAMEPERIODLASTYEAR ( Date_Table[Date] )
)

Rainfall YoY % =
DIVIDE (
  [Total Rainfall] - [Rainfall LY],
  [Rainfall LY]
)
