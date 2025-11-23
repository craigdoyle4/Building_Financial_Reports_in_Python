# 📊 Building Financial Reports Using Python  
*A data-driven financial analysis project using Python, Pandas, and Seaborn.*

## 📘 Overview  
This project demonstrates how to build automated, scalable financial reports using Python.  
The goal is to go beyond manual Excel work by programmatically merging financial statements, calculating core financial ratios, creating sector-level comparisons and visualising key relationships.

The workflow combines **Balance Sheet** and **Income Statement** data into a single, analysis-ready dataset. From there, it computes profitability and leverage metrics across multiple industries and presents them in a clear, repeatable way.

This project showcases the ability to  
- Handle and structure large, multi-source financial datasets  
- Apply core financial ratios in code  
- Perform sector-level comparisons  
- Automate reporting logic  
- Visualise financial relationships with regression plots  

---

## 🧾 Data & Processing Workflow  

### 1. Data Import and Merge  
Two Excel files are used as inputs  

- `Balance_Sheet.xlsx`  
- `Income_Statement.xlsx`  

Using `pandas`, these are merged into a unified DataFrame (`df_ratios`) on common keys  

- `Company`  
- `comp_type` (industry type)  
- `Year`  

This creates one table containing both income statement and balance sheet data for each company and year.

### 2. Calculating Key Financial Ratios  

Two core financial ratios are calculated for each company  

#### Gross Margin Ratio  
Formula  
```text
( Total Revenue - Cost Of Goods Sold ) / Total Revenue
