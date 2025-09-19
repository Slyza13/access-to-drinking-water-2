# Access to Drinking Water – Data Analysis Project 🌍💧

## Overview
This project analyzes **global access to safe and affordable drinking water** using the **WHO/UNICEF JMP Estimates on the Use of Water (2020)** dataset.  
It was completed as part of the **ALX Africa / ExploreAI Data Science Program**, aligning with **United Nations Sustainable Development Goal 6 (Clean Water and Sanitation).**

The work covers:
- Data import and cleaning
- Feature engineering
- Exploratory analysis
- Statistical summaries
- Data visualization
- Insights on access to water by area, population size, and income group

---

## 🚀 How to Navigate This Repo
- Start with **README.md** → gives you the big picture and results.  
- Look at **`/analysis/Project_1.xlsx`** → my cleaned dataset, calculations, and visualizations.  
- Explore **`/data/Estimates-on-the-use-of-water-2020.csv`** → raw dataset straight from WHO/UNICEF JMP.  
- Check **`/docs/Integrated-project-guidelines.pdf`** → the project brief from ALX/ExploreAI for context.  

---

## 📂 Repository Structure
📦 access-to-drinking-water
┣ 📂 data
┃ ┗ 📜 Estimates-on-the-use-of-water-2020.csv # Raw dataset (WHO/UNICEF JMP)
┣ 📂 analysis
┃ ┗ 📊 Project_1.xlsx # Cleaned + analyzed Excel file
┗ 📜 README.md # Project overview & documentation

---

## 📑 Files in this Repository

- **`/data/Estimates-on-the-use-of-water-2020.csv`**  
  Raw dataset from WHO/UNICEF JMP (Joint Monitoring Programme). Contains country-level water access estimates.

- **`/analysis/Project_1.xlsx`**  
  My working analysis file. Includes:
  - Data cleaning (delimiter fixes, missing values check, completeness count)  
  - Feature engineering (`pop_u_val`, `pop_r`, `pop_n (m)`, rounded indicators)  
  - Statistical summaries (mean, median, mode, IQR, std dev)  
  - Pivot tables and charts  

- **`/docs/Integrated-project-guidelines.pdf`**  
  Original project instructions provided by ALX/ExploreAI. Serves as the guideline for deliverables.  

- **`README.md`**  
  Documentation you are reading now.

---

## 🔎 Data Description
The dataset includes **16 original features**, such as:
- `name` → Country or area  
- `year` → Year of observation  
- `pop_n` → National population (in thousands)  
- `pop_u` → Urban population share (%)  
- Water access indicators (national, rural, urban):  
  - `wat_bas_*` = At least basic service (%)  
  - `wat_lim_*` = Limited service (%)  
  - `wat_unimp_*` = Unimproved service (%)  
  - `wat_sur_*` = Surface water only (%)  

**New features engineered:**
- `value_cnt` → Row completeness check  
- `pop_u_val` → Urban population count  
- `pop_r` → Rural population share (%)  
- `pop_n (m)` → Population in millions (rounded)  
- Rounded versions of access indicators (`wat_bas_n (rounded)`, `pop_u (rounded)`, etc.)  

---

## 📊 Analysis Highlights

1. **Population Comparison**  
   - Dataset total population vs. UN World Cities Report (2020): ~7.82B  
   - Urban share ~55% closely matches global estimates.  

2. **Water Access by Area**  
   - Urban areas show much higher access to basic water services.  
   - Rural areas lag significantly, with higher shares of unimproved/surface access.  

3. **Statistical Distributions**  
   - Distributions are skewed: most of the world has decent access, but outliers pull averages down.  
   - Boxplots reveal clear inequality between countries.  

4. **Population Size & Access**  
   - 100% stacked bar charts illustrate how national, rural, and urban population sizes affect service levels.  

5. **Income Group Analysis**  
   - Higher GNI = higher basic access.  
   - Low-income countries have the greatest share of limited, unimproved, and surface-level access.  
   - High-income countries approach universal basic access.  

---

## 📈 Visualizations
- **Line chart**: National population vs. urban & rural share  
- **Box-and-whisker plots**: Distribution of access levels across all features  
- **100% stacked column charts**: Water access by national, rural, and urban population size  
- **Pivot charts**: Water access vs. income group  

---

## 🌍 Key Insights
- **Global alignment:** Dataset matches world totals (~7.82B, 55% urban).  
- **Inequality:** Rural and low-income regions face the biggest challenges.  
- **Urbanization link:** Higher urbanization = better access.  
- **Income matters:** Economic development is a strong predictor of safe water access.  

---

## 🛠️ Tools Used
- **Microsoft Excel** → data cleaning, feature engineering, analysis, and visualization  
- **WHO/UNICEF JMP dataset (2020)**  

---

## 📚 Acknowledgement
This project was completed as part of the **ALX Africa / ExploreAI Data Science Program**.  
The dataset and project brief were provided by **ALX/ExploreAI**, and the analysis, feature engineering, visualizations, and interpretations were carried out by me.  

Dataset source: WHO/UNICEF Joint Monitoring Programme (JMP) – *Estimates on the Use of Water (2020)*.  

---

## 👤 Author
Project completed by **Sifiso Sibiya**, Data Scientist & Analyst.  
Focused on solving real-world problems in South Africa and globally 🌍.
