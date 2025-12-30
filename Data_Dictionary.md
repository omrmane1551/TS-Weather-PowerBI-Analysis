# 📘 Data Dictionary – TS Weather Data (2021–2024)

This document describes the structure and meaning of columns used in the **TS Weather Data Analysis Power BI Project**.

---

## 📊 Weather_Fact Table

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Date | Date | Date of weather observation |
| Avg Temperature | Decimal | Average temperature recorded for the day/month (°C) |
| Max Temperature | Decimal | Maximum temperature recorded (°C) |
| Min Temperature | Decimal | Minimum temperature recorded (°C) |
| Rainfall | Decimal | Total rainfall recorded (mm) |
| Year | Whole Number | Year extracted from the Date column |
| Month Name | Text | Month name derived from the Date column (January–December) |
| Month Number | Whole Number | Numeric representation of month (1–12), used for sorting |

---

## 📅 Date_Table (Calendar Dimension)

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Date | Date | Continuous calendar date |
| Year | Whole Number | Calendar year |
| Month Name | Text | Name of the month |
| Month Number | Whole Number | Numeric month (1–12) |
| Quarter | Text | Quarter of the year (Q1–Q4) |

---

## 🌡️ Measurement Units
- **Temperature:** Degrees Celsius (°C)
- **Rainfall:** Millimeters (mm)

---

## 🧹 Data Cleaning Notes
- Null and invalid records were removed in Power Query
- Column names were standardized across all CSV files
- Month Name is sorted using Month Number for correct chronological order
- Data from multiple years (2021–2024) was combined using Folder Connector

---

## 📌 Usage Notes
- The **Weather_Fact** table acts as the fact table
- The **Date_Table** is marked as a Date Table in Power BI
- All time-intelligence calculations (YoY, MoM) are based on the Date_Table

---

## ✅ Purpose of This Document
This data dictionary helps:
- Understand dataset structure quickly
- Improve collaboration and maintainability
- Demonstrate professional documentation practices

---
