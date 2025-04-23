# ☕ *Data Cleaning for Cafe*

This project aims to transform and clean data from a cafe by eliminating redundancies, improving data quality and persistency. It leverages data manipulation techniques using **Pandas**, with a focus on enhancing data integrity and optimizing storage for future analysis.

## 📌 Objectives

- Detect and remove duplicate or inconsistent records
- Convert invalid data types to numeric where applicable
- Replace or handle missing values
- Improve overall data structure and clarity

## 🛠️ Tools & Libraries

- Python
- Pandas
- Jupyter Notebook (for development and visualization)

## 🧼 Data Cleaning Steps

The dataset was cleaned and transformed incrementally, with each step saved as a `.pkl` file for reproducibility and version control.

### ✅ Checkpoints

- **data_step1.pkl**

  - Set all `Price Per Unit` values for each item correctly
  - Converted `Quantity`, `Price Per Unit`, and `Total Spent` to numeric types
  - Replaced non-numeric values with `NaN` (using `pd.to_numeric` with `errors='coerce'`)
  - Imputed missing values in `Quantity` by dividing `Total Spent` by `Price Per Unit`
  - Updated missing values in `Total Spent` by multiplying `Quantity` and `Price Per Unit`

- **data_step2.pkl**
  - Removed redundant or duplicate rows
  - Standardized column names (e.g., lowercase, underscores)
  - Trimmed whitespace in string values

- **data_step3.pkl**

- **data_step4.pkl**

  - Verified consistency in computed totals

### 🔄 File Naming Convention

Each step is saved as `data_stepN.pkl`, where `N` indicates the transformation phase.


## 💡 Key Learnings

- Data validation and type conversion using `pd.to_numeric()`
- Filtering rows with conditions (`isna()`, `notna()`)
- Creating new DataFrames from cleaned Series
- Good practices in data preprocessing for analysis

## 📁 Output

The final cleaned DataFrame is ready for further use in dashboards, analysis, or machine learning tasks.

---

Feel free to fork or use it as a reference in your own data projects!

