#  Data Cleaning & Preparation Steps

This document describes how the raw retail sales data (2018–2021) was prepared for analysis and dashboarding in Excel.

The goal of the cleaning process was to:
- Ensure **data quality and consistency**
- Create **analysis-ready fields** (e.g., Profit Margin %, Year)
- Enable **pivot-based KPIs and charts** for the Executive Sales & Profit Dashboard

---

## 1️ Import & Initial Checks

1. Imported the raw transactional dataset into Excel from the source file.
2. Verified the presence of all expected fields:
   - Order ID, Order Date, Sales, Profit, Quantity / Order Count  
   - Category, Sub-Category, Segment, Region  
   - Returned Orders (if available)  
3. Checked for:
   - Blank rows / columns  
   - Obvious structural issues (merged cells, totals rows, etc.)  
4. Removed any **summary / total rows** that could interfere with PivotTables.

---

## 2️ Handling Missing & Invalid Data

1. Filtered each column to check for:
   - Missing Order IDs  
   - Missing Order Dates  
   - Negative or zero Sales values (where not expected)  
2. For records with **missing critical fields** (Order ID, Date, Sales):
   - Excluded them from the analysis dataset.
3. Ensured Quantity values were positive and numeric.
4. Verified that Category, Segment, and Region values matched expected lists.

---

## 3️ Data Type & Format Standardisation

1. Converted **Order Date** column to proper Excel Date format.
2. Ensured:
   - Sales and Profit → Number with 2 decimal places  
   - Quantity → Whole Number  
3. Standardised text fields (Category, Segment, Region) by:
   - Trimming extra spaces  
   - Correcting any inconsistent spellings / casing  
4. Confirmed Region values aligned with: **East, West, South, Central**.

---

## 4️ Creating Derived Columns

To support KPI calculations and pivot analysis, the following new fields were created:

1. **Year**
   - Extracted from `Order Date` using Excel formula (e.g., `=YEAR([@Order_Date])`).
   - Used for time-series analysis and slicer filtering (2018–2021).

2. **Profit Margin %**
   - Formula:  
     `Profit Margin % = Profit ÷ Sales × 100`
   - Used to compare profitability across products, regions, and segments.

3. **Returned Orders Flag** (if stored separately)
   - Normalised into a 0/1 field (1 = returned, 0 = not returned).
   - Used to calculate **Return Rate %** and build return analysis charts.

---

## 5️ Preparing the Analysis Table

1. Converted the cleaned data range into an **Excel Table**:
   - This makes formulas and pivots dynamic and easy to refresh.
2. Gave the table a clear name (e.g., `tbl_SalesData`).
3. Verified row and column counts after cleaning:
   - Confirmed that all relevant records from 2018–2021 were retained.

---

## 6️ Loading Data into PivotTables

1. Used the cleaned table (`tbl_SalesData`) as the source for all PivotTables.
2. Built multiple PivotTables for:
   - KPI calculations  
   - Segment-wise and Region-wise analysis  
   - Category and Sub-Category performance  
   - Salesperson performance (where available)
3. Connected these PivotTables to dashboard charts and slicers.

---

## 7️ Quality Check Before Dashboarding

1. Manually checked a few sample orders to confirm:
   - Profit and Profit Margin % calculations are correct.
   - Totals from PivotTables match the underlying data.
2. Tested slicers (Year, Region, Segment) to ensure all values respond correctly.
3. Verified that no blank or “error” categories appear in charts or KPIs.

---

By the end of this process, the dataset was:
- Clean, consistent, and analysis-ready  
- Structured to support **pivot-driven KPIs and visualisations**  
- Fully aligned with the requirements of the Executive Sales & Profit Dashboard
