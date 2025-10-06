# 🎬 Movie Data Cleaning in Excel

## 📘 Overview
This project focuses on cleaning and preparing a raw movie dataset containing over **10,000 records** using **Microsoft Excel**.  
The goal is to transform messy, inconsistent, and incomplete data into a structured, analysis-ready format for further **Exploratory Data Analysis (EDA)**.

## ⚠️ Disclaimer
Before performing **EDA (Exploratory Data Analysis)**, please **recheck the dataset**.  
Although extensive cleaning has been performed, complex datasets may still contain subtle inconsistencies, missing values, or format variations that cannot be fully automated.  
It is recommended to **validate and cross-check the cleaned data from your end** before proceeding with analysis.


---

## 🧹 Data Cleaning Approach
A systematic data cleaning process was applied to ensure data accuracy, consistency, and usability.

### **1. Remove Duplicates**
All duplicate entries across columns were identified and removed to maintain data integrity and ensure each record is unique.

---

### **2. Standardize Year Format**
- Corrected inconsistent year formats and removed unwanted characters or encoding errors (e.g., `â€“`).
- Extracted clean year values from mixed text formats (e.g., `(I) (2013–2016)` → `2013–2016`).
- Filled missing or null year values with **“N/A”** or **“Unknown”** for clarity.

---

### **3. Handle Missing Values — Genre**
Blank or missing entries in the **Genre** column were replaced with **“Unknown”** to ensure categorical completeness.

---

### **4. Handle Missing Values — Rating**
- Missing ratings were replaced with **0** to maintain numeric consistency for EDA.  
- A value of **0** represents **“Not Rated / Missing”**, allowing statistical summaries (mean, median, histograms) to be calculated without data type errors.

---

### **5. Handle Missing Values — Votes**
- Blank cells in the **Votes** column were replaced with **0**, representing **“No Votes Recorded.”**  
- This preserves numeric consistency for aggregation and ensures valid numeric data during visualization and analysis.

---

### **6. Handle Missing Values — Runtime**
- Blank runtime entries were replaced with **“0”**, indicating unavailable duration information without affecting numeric summaries.

---

### **7. Handle Missing Values — Gross**
- Missing or undisclosed box office figures were replaced with **0 = “Not Disclosed”**.  
- The numeric 0 ensures data type consistency, while the **“Not Disclosed”** label clarifies the meaning of missing data.

---

### **8. Split “Stars” Column**
- The **Stars** column contained both **Director** and **Cast** details in a single field.  
- This column was **split into two new columns**:
  - **Director**
  - **Stars (Main Cast)**
- Missing values in either were filled with **“Unknown”** to maintain completeness and avoid nulls during analysis.

---

## 🧠 Meaning of Replacement Values

| Column | Replacement | Meaning / Purpose |
|---------|-------------|------------------|
| **Year** | `Unknown / N/A` | Year not specified |
| **Genre** | `Unknown` | Genre missing |
| **Rating** | `0` | Not rated / missing (numeric consistency) |
| **Votes** | `0` | No votes recorded |
| **Runtime** | `0` | Runtime unavailable |
| **Gross** | `0 = Not Disclosed` | Gross not shared |
| **Director / Stars** | `Unknown` | Information missing |

---

## ✅ Final Outcome
- Cleaned and structured dataset with no duplicates or blanks.  
- Numeric fields standardized for analysis.  
- Text columns formatted consistently (trimmed, proper case applied).  
- Dataset is now **analysis-ready** for dashboards, visualizations, or further data exploration.

---



