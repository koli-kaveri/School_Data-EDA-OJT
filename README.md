# School Dataset - Exploratory Data Analysis (EDA)

> **OJT Project | MSc Data Science**

---

## Project Overview

This project performs a complete Exploratory Data Analysis (EDA) on a real-world school dataset containing **5200 schools** across 3 districts.

The goal is to understand what factors affect student performance and build a basic prediction model.

---

## Files in this Repository

| File | Description |
|------|-------------|
| `School_EDA_Simple.ipynb` |  Main Jupyter Notebook with full EDA + simple comments |
| `School_data.xlsx` | Raw dataset (school data) |
| `School_EDA_Summary.txt` | Short written summary of findings |
| `requirements.txt` | Python libraries needed to run the notebook |
| `README.md` | This file - explains the project |

---

##  Dataset Info

| Property | Value |
|----------|-------|
| Total Rows | 5,200 |
| Total Columns | 17 |
| Districts | District_A, District_B, District_C |
| School Types | Urban, Rural |

**Columns include:**
- `%_Math_Score`, `%_Language_Score`, `%_Science_Score` - student scores
- `Teacher_Student_Ratio`, `Avg_Teacher_Experience_Years` - teacher info
- `Electricity_Available`, `Internet_Available`, `Library_Available` - infrastructure
- `Parent_Literacy_Rate`, `%_Marginalized_Students` - community factors

---

## Steps Performed

### 1. Data Understanding
- Loaded dataset and checked shape, types, and statistics

### 2. Data Cleaning
- Filled missing values using **median** (robust to outliers)
- Fixed out-of-range values (scores capped to 0–100)
- Checked and confirmed no duplicate rows

### 3. Exploratory Data Analysis
- **Univariate:** Score distributions, Urban vs Rural count, Infrastructure availability
- **Bivariate:** Urban vs Rural scores, District-wise comparison, Parent literacy effect
- **Correlation:** Heatmap of all numeric columns

### 4. Key Insights
1. Urban schools score higher than Rural schools
2. Parent literacy positively affects student scores
3. Poor infrastructure leads to poor scores
4. Math, Language, Science scores are all correlated
5. Higher % of marginalized students = lower scores
6. Teacher experience alone has weak effect on scores

### 5. ML Model
- Created new features: `Avg_Score`, `Infra_Score`, `Is_Urban`
- Built a **Linear Regression** model to predict average school score
- Evaluated using R² Score and MAE

---

## How to Run

### Step 1 - Install libraries
```bash
pip install -r requirements.txt
```

### Step 2 - Open the notebook
```bash
jupyter notebook SchoolData_EDA.ipynb
```

### Step 3 - Run all cells
Go to **Kernel → Restart & Run All**

>  Make sure `School data.xlsx` is in the **same folder** as the notebook!

---

## Libraries Used

| Library | Purpose |
|---------|---------|
| `pandas` | Load and clean data |
| `numpy` | Math operations |
| `matplotlib` | Draw graphs |
| `seaborn` | Nicer-looking graphs |
| `scikit-learn` | Build ML model |

---

##  About

- **Type:** OJT (On-the-Job Training) Project
- **Domain:** Data Science
- **Tools:** Python, Jupyter Notebook

---
