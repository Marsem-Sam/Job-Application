# 💳 Credit Card Transactions - Data Engineering Assessment

**Author:** Sammuel  
**Date:** July 10, 2025

## 📌 Objective

This notebook demonstrates a PySpark-based data engineering pipeline to clean, transform, and analyze messy credit card transaction data. The original dataset had only one record, so dummy records were generated to simulate realistic data patterns and facilitate meaningful analysis.

---

## 📖 Workflow Summary

### 🔹 Step 1: Load JSON Data
- Load the original JSON transaction record
- Generate dummy records to supplement the data
- Merge real and dummy data using `union()`

### 🔹 Step 2: Flatten the JSON Structure
- Parse nested fields in `personal_detail`
- Extract subfields like gender, location, and job
- Keep address as a string for later parsing

### 🔹 Step 3: Extract Name Components
- Parse `person_name` to derive first and last names for downstream enrichment

### 🔹 Step 4: Timestamp Standardization
- Convert all transaction timestamps to **UTC+8** timezone using PySpark datetime functions

### 🔹 Step 5: PII Masking
- Redact or hash sensitive fields such as credit card numbers (`cc_num`) for compliance and security

### 🔹 Step 6: Data Exploration & Visualization
- Perform exploratory data analysis (EDA)
- Create visualizations to highlight spending behavior, fraud patterns, and category distributions

---

## 📂 Project Structure

```
credit_card_data_assessment.ipynb     # Main notebook with PySpark ETL and visualizations
data/                                 # (Optional) Place for external or generated data
README.md                             # This file
```

---

## 🛠️ Technologies Used

- **PySpark** for scalable ETL and transformations  
- **Pandas** for small-scale data inspection  
- **Matplotlib / Seaborn** for data visualization  
- **Jupyter Notebook** as the development environment

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Spark 3.x with PySpark installed
- Jupyter Notebook or compatible IDE (e.g., VSCode, Databricks)

### Run the Notebook

1. Clone the repository or open the notebook locally
2. Ensure Spark is configured correctly
3. Run each cell sequentially

---

## 📈 Sample Output

- Cleaned transaction data with parsed fields
- Time-normalized events in UTC+8
- Visual dashboards showcasing fraud detection and spending insights

---

## 📌 Notes

- Dummy data was generated to simulate diverse conditions due to insufficient source data
- Address parsing is optional and kept as a placeholder
