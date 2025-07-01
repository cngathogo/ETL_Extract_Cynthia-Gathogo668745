### 📘 Notebook Description

This notebook performs both **full and incremental extraction** of a dataset using simulated timestamps. It loads a dataset, displays basic statistics, simulates a last extraction time, and filters for new or updated records since the last extraction.

---

### 🛠️ Tools Used

- **Python**
- **pandas**
- **Jupyter Notebook**
- **Git** (for version control)

---

### 🔁 How to Reproduce

#### ▶️ How to Run:
1. Open `etl_extract.ipynb` in Jupyter.
2. Run all cells in sequence.
3. The `last_extraction.txt` keeps track of the last extraction time, updating anytime a change is made.

#### 📊 Where the Data Comes From:
- The sample dataset is from **Kaggle** 
- a timestamp column was added to make the dataset suitable for the task

---


---

## Lab 5 – Load

### ✅ Loading Method Used

- **SQLite Database**
- Implemented using Python’s built-in `sqlite3` and Pandas `to_sql()`.

### 📥 Loaded Targets

- `loaded_data/full_data.db` – from `transformed_full.csv`
- `loaded_data/incremental_data.db` – from `transformed_incremental.csv`

### 💾 Schema Used

```sql
CREATE TABLE full_data (
    id INTEGER PRIMARY KEY,
    customer_name TEXT,
    product TEXT,
    quantity INTEGER,
    unit_price REAL,
    total_price REAL,
    order_date TEXT
);



