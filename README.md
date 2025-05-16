# 💓 Heart Disease Prediction - Databricks Project

This project performs end-to-end data analysis on the Kaggle Heart Disease dataset using **Apache Spark**, **Databricks**, **Delta Lake**, and **Python**. The objective is to clean, explore, and extract insights from the dataset to understand factors that influence the presence of heart disease.

---

## 💾 Dataset

- **Source**: [Kaggle - Heart Disease Data](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)
- **Records**: 920 patient entries
- **Features**: Demographics, ECG readings, cholesterol, chest pain, heart rate, and more

---

## 🧪 Workflow Overview

### 1. 📥 Data Ingestion
- Loaded the dataset into a Spark DataFrame.
- Defined schema explicitly for performance and consistency.
- Saved data in **Delta format** to **Databricks File System (DBFS)**.

### 2. 🧹 Data Cleaning
- Removed duplicates using the `id` column.
- Imputed missing values:
  - Numerical features like `chol`, `trtbps`, `thalach`, and `oldpeak` were filled using mean.
  - Categorical columns like `restecg`, `exang`, and `fbs` were handled with mode or domain logic.
- Renamed the target column `stage` for better clarity.

### 3. 📊 Data Exploration
- Converted Spark DataFrame to Pandas for visualization.
- Created charts using **Matplotlib** and **Seaborn**:
  - Pair plots, heatmaps, count plots, and scatter plots.
- Analyzed correlations and distributions of heart health indicators.

---

## 📈 Key Insights

### 🧍 Demographics
- Most patients are aged between **50–60 years**.
- **Male patients** show a higher prevalence of heart disease.

### ❤️ Clinical Observations
- **Max Heart Rate (`thalachh`)**: Negatively correlated with heart disease. Higher rates are typical in healthier individuals.
- **Exercise-Induced Angina (`exng`)**: More frequent among patients with heart disease.
- **Oldpeak (ST Depression)**: Higher `oldpeak` values correlate with greater disease severity.

### 🧪 ECG and Other Factors
- **Cholesterol & Resting BP**: Do not show strong correlation individually with the target variable.

---

## 🔧 Tech Stack

- [Databricks](https://www.databricks.com/)
- Apache Spark (PySpark)
- Delta Lake
- Python
- Pandas
- Seaborn / Matplotlib

---

## 🚀 How to Run

1. Upload the Kaggle dataset CSV to Databricks File System (DBFS).
2. Run notebooks in the following order:
   - **Data Ingestion**
   - **Data Cleaning**
   - **Data Exploration**
3. Use a cluster with Spark and Python support.

---

## 📚 References

- [Kaggle Dataset](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)
- [Databricks Docs](https://docs.databricks.com/)
- [Seaborn Docs](https://seaborn.pydata.org/)

---

## 📌 Author

Aditya Pani — *Data Analyst passionate about solving real-world problems with data.*

