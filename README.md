![Excel](https://img.shields.io/badge/Tool-Excel-green) 
![Google Sheets](https://img.shields.io/badge/Tool-GoogleSheets-blue) 
![ALX Africa](https://img.shields.io/badge/Project-ALX-yellow)

# 🌍 Integrated Project 2 – Global Water Access (2000–2020)

---

## 📢 Acknowledgement
This project is part of the **Integrated Project 2** under **[ALX Africa / Explore AI](https://www.alxafrica.com/)**.  
We thank ALX and Explore AI for providing the datasets and project guidelines that made this analysis possible. 🙏

---

## 📌 Table of Contents
1. [Overview](#-overview)
2. [Datasets](#-datasets)
3. [Analysis Steps (Google Sheets)](#-analysis-steps-google-sheets)
4. [Key Insights](#-key-insights)
5. [Tools & Techniques](#-tools--techniques)
6. [Deliverables](#-deliverables)
7. [References](#-references)
8. [Notes](#-notes)

---

## 🔹 Overview
This project analyzes **country-level data on water access and population** using **Google Sheets**. It covers observations from **2000–2020**, focusing primarily on **2015 and 2020**.  

The goal is to **transform raw data into actionable insights**, highlighting trends, disparities, and progress toward **UN Sustainable Development Goal 6: Clean Water and Sanitation**.  

We calculate **Annual Rates of Change (ARC)**, compare **rural vs urban access**, and summarize trends at both **national and regional levels**.

---

## 📁 Datasets

### 1️⃣ Raw Data – [Analysis Folder](./analysis)
- **Estimates of the use of water (2000-2020).csv**  
  Country-level water access and population data.  
  **Columns include**:
  - `name` – Country or region name  
  - `year` – Observation year (e.g., 2015, 2020)  
  - `pop_n`, `pop_u` – National and urban population  
  - **Water access metrics**:
    - `wat_bas_n/r/u` – Basic water services  
    - `wat_lim_n/r/u` – Limited services  
    - `wat_unimp_n/r/u` – Unimproved sources  
    - `wat_sur_n/r/u` – Surface water  
  - **Calculated fields**:
    - `year_difference` – Gap between consecutive entries per country  
    - `arc_n/r/u` – Annual Rate of Change for national, rural, urban populations  
    - Rounded access metrics and full access flags (`arc_n_full`, etc.)  
    - `arc_diff` / `Absolute Diff` – Differences between rural and urban access  

- **Regions.csv**  
  Maps each country to a **geographic region** (e.g., Sub-Saharan Africa, Europe).  

---

### 2️⃣ Project 2 Work – [Data Folder](./data)
- **Transformed_Dataset.xlsx** – Raw dataset enhanced with calculated fields, ARC metrics, rounded access, full access flags, and regional identifiers.  
- **Summary_Report.xlsx** – Aggregated statistics for national, rural, and urban populations; regional summaries and visualizations; key insights.

---

## 🔹 Analysis Steps (Google Sheets)

1. **Inspect & Clean Data**  
   - Reviewed dataset structure, removed duplicates, ensured consistent country names.  

2. **Calculate Year Differences**  
   - Created `year_difference` to measure gaps between consecutive entries.  

3. **Compute Annual Rate of Change (ARC)**  
   - Formula:  
     ```
     ARC = (Value in Year n+1 – Value in Year n) / Year Difference
     ```
   - Applied to national, rural, and urban populations (`arc_n/r/u`).  
   - Used `IFERROR` to handle missing/null values.  

4. **Round & Flag Full Access**  
   - Rounded percentages ≥100% to define **full access**.  
   - Created flags like `arc_n_full`, `arc_r_full`, `arc_u_full`.  

5. **Compare Rural vs Urban Access**  
   - Calculated `arc_diff = arc_r - arc_u` to identify rural progress relative to urban.  
   - Visualized disparities with histograms.  

6. **Summarize by Region**  
   - Merged `Regions.csv` using `VLOOKUP`.  
   - Calculated average ARC and population-weighted access per region.  
   - Scatter plots comparing national vs rural progress.  

7. **Generate Final Summary Sheet**  
   - Compiled transformed columns, ARC metrics, and regional insights into **“Global 2000–2020 Report”**.  
   - Highlighted key findings, including slow progress in **Sub-Saharan Africa**.  

---

## 📊 Key Insights

- **Sub-Saharan Africa** lags in achieving universal basic water access.  
- Rural populations are improving in some countries, but urban areas generally have higher access.  
- If current trends continue, some countries may take decades to reach full access (~2080).  
- ARC metrics and visualizations reveal **improvement, stagnation, and decline** patterns across regions.  

---

## 🛠 Tools & Techniques

- **Platform:** Google Sheets  
- **Formulas Used:**  
  - `IF`, `IFERROR` → Conditional calculations and error handling  
  - `ROUND` → Define full access  
  - `VLOOKUP` → Merge regional information  
  - Arithmetic → Calculate ARC and differences  

---

## ⚡ Deliverables

1. **Transformed Dataset** – Original dataset + calculated fields (28 columns total).  
2. **Summary Report** – Aggregated statistics and visualizations, highlighting key insights.

---

## 🔗 References

- **WHO/UNICEF JMP** – Water Supply and Sanitation  
- **UN Sustainable Development Goal 6** – Clean Water and Sanitation  

---

## 💡 Notes

- Many columns contain **Excel formulas** (`IF`, `IFERROR`, `ROUND`) to handle missing data and categorize access.  
- Some observations have `null` values.  
- Country name consistency is crucial for merging datasets.  

