# 🌍 Integrated Project Part 2 – Global Water Access (2000–2020)

---

## 📢 Acknowledgement
This project is part of the **Integrated Project 2** under **[ALX Africa / Explore AI](https://www.alxafrica.com/)**.  
🙏 Big thanks to ALX and Explore AI for the datasets and project guidance!

---

## 🌟 Badges
![Excel](https://img.shields.io/badge/Tool-Excel-green)
![Google Sheets](https://img.shields.io/badge/Tool-GoogleSheets-blue)
![Data Analysis](https://img.shields.io/badge/Skill-DataAnalysis-yellow)
![ALX Africa](https://img.shields.io/badge/Project-ALX-red)

---

## 📌 Table of Contents
1. [Project Description](#-project-description)
2. [Datasets](#-datasets)
3. [Analysis Steps (Google Sheets)](#-analysis-steps-google-sheets)
4. [Key Insights](#-key-insights)
5. [Tools & Techniques](#-tools--techniques)
6. [Deliverables](#-deliverables)
7. [References](#-references)
8. [Notes](#-notes)

---

## 📖 Project Description
> 🌊 Turning raw water access data into actionable insights!  
> This project tracks **national, rural, and urban water access** for countries worldwide from **2000–2020**, highlighting trends, disparities, and regional progress toward **SDG 6: Clean Water and Sanitation**.

---

## 📁 Datasets

### 1️⃣ Raw Data – [Analysis Folder](./analysis)
- **Estimates of the use of water (2000-2020).csv**  
  Country-level water access and population data.  

- **Regions.csv**  
  Maps countries to geographic regions (e.g., Sub-Saharan Africa, Europe).  

**Columns of Interest**:
| Column | Description |
|--------|-------------|
| `name` | Country or region name |
| `year` | Observation year (e.g., 2015, 2020) |
| `pop_n`, `pop_u` | National and urban population |
| `wat_bas_n/r/u` | Basic water services |
| `wat_lim_n/r/u` | Limited services |
| `wat_unimp_n/r/u` | Unimproved sources |
| `wat_sur_n/r/u` | Surface water |
| `arc_n/r/u` | Annual Rate of Change |
| `arc_diff` | Rural vs Urban access difference |
| `arc_n/r/u_full` | Full access flags |

---

### 2️⃣ Project 2 Work – [Data Folder](./data)
- **Transformed_Dataset.xlsx** – Dataset with all calculated fields, ARC metrics, rounded access, and regional identifiers.  
- **Summary_Report.xlsx** – Aggregated statistics, regional summaries, visualizations, and insights.  
---

## 🔹 Analysis Steps (Google Sheets)

<details>
<summary>Click to expand Step-by-Step</summary>

1. **Inspect & Clean Data**  
   - Remove duplicates, handle nulls, standardize country names.  

2. **Calculate Year Differences**  
   - `year_difference` → gap between consecutive entries per country.  

3. **Compute Annual Rate of Change (ARC)**  
   - Formula:  
     ```
     ARC = (Value in Year n+1 – Value in Year n) / Year Difference
     ```
   - Applied to national, rural, and urban populations (`arc_n/r/u`).  
   - Used `IFERROR` to handle missing/null values.  

4. **Round & Flag Full Access**  
   - Rounded percentages ≥100% = full access.  
   - Flags: `arc_n_full`, `arc_r_full`, `arc_u_full`.  

5. **Compare Rural vs Urban Access**  
   - `arc_diff = arc_r - arc_u`  
   - Histograms to visualize disparities.  

6. **Summarize by Region**  
   - Merged `Regions.csv` using `VLOOKUP`.  
   - Average ARC and population-weighted access per region.  
   - Scatter plots comparing national vs rural progress.  

7. **Generate Final Summary Sheet**  
   - Compiled transformed columns, ARC metrics, and regional insights.  
   - Highlighted key findings for advocacy.  

</details>

---

## 📊 Key Insights
- **Sub-Saharan Africa** lags in universal basic water access.  
- Rural populations improve in some countries, but urban areas generally lead.  
- Current trends suggest decades before full access (~2080).  
- ARC metrics reveal patterns of **improvement, stagnation, and decline**.  

---

## 🛠 Tools & Techniques
- **Platform:** Google Sheets  
- **Formulas Used:** `IF`, `IFERROR`, `ROUND`, `VLOOKUP`  
- **Analysis:** Year differences, ARC, rural vs urban comparison, regional summaries  

---

## ⚡ Deliverables
1. **Transformed Dataset** – Original + calculated fields (28 columns).  
2. **Summary Report** – Aggregated statistics, visualizations, key insights.  

---

## 🔗 References
- **WHO/UNICEF JMP** – Water Supply and Sanitation  
- **UN Sustainable Development Goal 6** – Clean Water and Sanitation  

---

## 💡 Notes
- Columns contain **Excel formulas** (`IF`, `IFERROR`, `ROUND`) to handle missing data and categorize access.  
- Some observations have `null` values.  
- Consistency in country names is crucial for merges.  

---



