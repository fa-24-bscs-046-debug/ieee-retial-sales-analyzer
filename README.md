# Retail Sales Intelligence
### IEEE LGU AI/ML Cohort One — Fall 2026
**Week 3 Assignment:** Data Analysis with NumPy & Pandas
**AI/ML Leads:** Abdullah Faisal & Alina Irshad

---

## 1. Project Overview
- Analyzes raw September 2026 sales records from `data/sales.csv`.
- Cleans bad rows, computes revenue metrics with NumPy.
- Ranks products, categories and regions with `groupby`.

## 2. Key Concepts Implemented
- [x] Pandas DataFrame Loading & Cleaning (`read_csv`, `fillna`, `dropna`, `drop_duplicates`)
- [x] NumPy Statistical Calculations (Mean, Median, Standard Deviation, Sums)
- [x] Data Grouping & Aggregation (`groupby`)
- [x] Conditional Filtering & Indexing

## 3. How to Run the Program
```shell
pip install pandas numpy
python main.py
```


## 4. Dataset Information & Cleaning Decisions
- **Data Source:** Self-made realistic CSV with intentional errors.
- **Duplicate `order_id`:** kept first record only.
- **Invalid date:** row dropped.
- **Units sold** (`abc`, missing, ≤ 0): row dropped — quantity can't be guessed.
- **Unit price** (missing or negative): filled with the median price of the same product.
- **Text columns:** whitespace and case normalised (`" north"` → `North`).
- **Revenue:** `np.multiply(units_sold, unit_price)`; AOV = total revenue ÷ unique orders.

## 5. Console Output Screenshots
**Data cleaning log**

![Cleaning Output](screenshots/cleaning_output.png)

**Summary report**

![Terminal Output](screenshots/summary_report.png)
