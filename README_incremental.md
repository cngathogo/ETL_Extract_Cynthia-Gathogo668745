# 🧪 ETL Project – Data Transformation

## 📄 Project Overview
This project demonstrates an ETL pipeline using a medical dataset. The main focus is on transforming both full and incremental data extracts.

## 📁 Files
- `📌 transformed_full.csv`: Fully transformed dataset with all 299 records.
- `📌 transformed_incremental.csv`: Supposed to contain only new or updated records — but currently contains all 299 due to uniform timestamps.

## 🔧 Transformations Applied
✅ **Cleaning**
- Removed duplicate records  
- Replaced missing values with zeroes

✅ **Enrichment**
- Added `risk_score`:  
  `risk_score = (serum_creatinine * age) / ejection_fraction`

✅ **Structural**
- Converted `timestamp` to datetime  
- Ensured correct data types (e.g., `age` as integer)

✅ **Filtering**
- Dropped the `smoking` column

✅ **Categorization**
- Binned `age` into: `<30`, `30–45`, `45–60`, `60–75`, `75+`

## ⚠️ Note on Incremental Data
All rows in the dataset have the **same timestamp** (`2025-06-10`).  
📌 This means filtering by date didn’t reduce the data — so the incremental file contains all rows just like the full dataset.

