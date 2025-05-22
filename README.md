# 📊 AdventureWorks Sales Analysis (Power BI Intermediate Project)
***2nd Level to a beginner Power BI Project - self working***

This repository showcases an intermediate-level Power BI project based on the AdventureWorks Sales dataset. The project demonstrates the transition from raw flat data into a structured star schema model, the use of both Power Query and DAX for calculations, and the comparison of their outputs. It focuses on deriving ***profitability insights*** through effective data modeling, cleaning, and visualization.

## 📂 Files Included

- 🟨 **Adventure Works Sales [Intermediate].pbix**  
  Power BI project file containing all data transformations, relationships, DAX measures, and visuals.

- 📄 **Adventure Works Sales [Intermediate] Problem Statement.docx**  
  Document outlining the problem statement, step-by-step process, and solutions.

- 📊 **AdventureWorks_Sale_2.xlsx**  
  Source dataset with sales, customer, product, date, and territory details.

## 📁 Dataset Overview

The dataset mimics operations of *Adventure Works Cycles*, a fictional multinational manufacturing company. It includes:
- Sales Transactions  
- Product Information  
- Customer Data  
- Date and Territory Tables

## ⚙️ Core Project Steps

### 🔗 Data Modeling
- Converted the dataset into a **star schema**.
- Created a **1-to-Many relationship** between `Date[DateKey]` and `Sales[DueDateKey]`.

### 🧹 Data Cleaning & Transformation (Power Query)
- Checked column data types, removed nulls and duplicates.
- Promoted headers, ensured column quality and consistency.
- Created a calculated column `Profit_Que_Edi` as:  
  `Profit_Que_Edi = [Sales Amount] - [Total Product Cost]`
- Rounded `Profit_Que_Edi` to **two decimal places**.

### 📐 Calculations with DAX
- Created `Profit_cal_col` using:  
  `Profit_cal_col = Sales[Sales Amount] - Sales[Total Product Cost]`
- Created aggregate measures using:
  - `SUM()` – Column-level aggregation
  - `SUMX()` – Row-level aggregation  
  > Both yielded identical results in this dataset due to structure and granularity.

- Converted customer names to uppercase using:  
  `UPPER([Customer Name])`

### 📊 Visual Analysis
- Built visuals comparing:
  - `Profit_Que_Edi` (Power Query) vs. `Profit_cal_col` (DAX)
- Used **date hierarchy** in charts for drill-down from year to day level.
- Displayed measures using:
  - Table visualizations
  - Clustered column charts

## 🧠 What You'll Learn

- How to convert raw Excel data into a clean, analytical model.
- Differences between **Power Query vs. DAX** for transformations.
- Behavior of `SUM()` vs. `SUMX()` in DAX calculations.
- Best practices for modeling and designing star schemas in Power BI.
- Hierarchical drill-down and comparative visual reporting.

## 🛠 Tools & Technologies

- **Power BI Desktop**
- **Power Query Editor**
- **DAX (Data Analysis Expressions)**
- **Excel Workbook (.xlsx)**

## 🏷 Tags

`Power BI` `Intermediate Project` `Power Query` `DAX` `Data Modeling`  
`Profit Analysis` `Sales Dashboard` `Star Schema` `AdventureWorks`

## 👤 Author

**Bidarth Kr. Singh**

## 📌 Credits

        This project was created by Bidarth Kr. Singh and is distributed under the "Apache License" license.

# Snapshot of Dashboard

![Image](https://github.com/user-attachments/assets/4c38177e-8a17-42aa-be3b-01624357a2a3)

---
