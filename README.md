# Analysis on Alzheimer’s Disease and Healthy Aging Data

This project involves performing **Exploratory Data Analysis (EDA)** on publicly available datasets related to Alzheimer's disease and healthy aging. It aims to uncover patterns, trends, and insights that may help raise awareness and support early detection and care planning.

---

## 📌 Problem Statement

**"Raising awareness about Alzheimer’s disease and promoting healthy aging practices to improve quality of life and support early detection."**

---

## 🎯 Objectives

- Explore and understand the structure of Alzheimer’s datasets.
- Handle missing data and perform data cleaning and reduction.
- Analyze the impact of age, region, and time period on Alzheimer’s trends.
- Visualize key patterns related to caregiving, mental health, and regional prevalence.

---

## 🧾 Dataset Description

- **Source**: [Alzheimer’s Disease and Healthy Aging Data (Data.gov)](https://catalog.data.gov/dataset/alzheimers-disease-and-healthy-aging-data)
- **Years Covered**: 2015–2022
- **Shape (Raw)**: 250,937 rows × 31 columns  
- **Shape (After Cleaning)**: 99,114 rows × 29 columns

---

## ⚙️ Preprocessing Steps

Major tasks of data preprocessing applied to our dataset:
- Data Cleaning
- Data Reduction

🔹 Data Cleaning
- Checked for missing values using .isnull().sum() and .isna().any(axis=1)
- Filled missing values:
- Used .fillna(mean) for numerical columns with normally distributed data (e.g., Data_Value)
- Used .fillna(mode) for categorical or discrete numeric columns (e.g., Low_Confidence_Limit, High_Confidence_Limit)
- Verified that columns like Data_Value_Footnote and Data_Value_Footnote_Symbol had a very high proportion of nulls

🔹 Data Reduction
- Dropped columns:
Data_Value_Footnote and Data_Value_Footnote_Symbol were removed due to excessive missing values (~151,823 nulls out of 250,937 records)

- Merged columns:
Combined LocationAbbr and LocationDesc for better regional interpretation

Final dataset shape:
- Before preprocessing: 250,937 rows × 31 columns
- After preprocessing: 99,114 rows × 29 columns

---

## 📊 Key Findings

- **Year with highest cases**: 2016  
- **Most affected age group**: 65+  
- **Dominant class ID**: `C07` – Caregiving  
- **Top topic**: Providing care to someone with cognitive impairment  
- **Region with most cases**: Southern United States (`SOU`)

---

## 📈 Visualizations Used

- Cases per year
- Cases by region
- Age group impact
- Class ID and topic distribution
- Histogram comparisons and confidence intervals

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.


