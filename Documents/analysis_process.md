#  Analysis & Dashboard Development Process

This document outlines the full analytical workflow used to build the **Executive Sales & Profit Dashboard (2018–2021)**, including KPI development, pivot modelling, visualization logic, and dashboard layout design.

---

## 1️ KPI Creation & Business Metrics

The dashboard highlights eight core KPIs, each created using PivotTables and GETPIVOTDATA for dynamic linkage.

### **KPIs Implemented**
- **Total Sales** – Σ(Sales)
- **Total Profit** – Σ(Profit)
- **Total Orders** – Σ(Order Count)
- **Return Rate (%)** – (Returned Orders ÷ Orders) × 100
- **Average Profit per Order**
- **Buyer Segment Margin (%)**
- **Region Segment Margin (%)**
- **Top Seller & Product Category**

These KPIs support executive decision-making by summarizing:
- Revenue performance  
- Profitability efficiency  
- Customer segment behaviour  
- Regional health  
- Product/category contribution  


---

## 2️ Pivot Modelling

Multiple PivotTables were created to act as data engines for the dashboard.

### **PivotTables Included**
- Sales & Profit summary by Year
- Segment-wise Profitability (Consumer, Corporate, Home Office)
- Region-wise Profit Margin (East, West, South, Central)
- Category/Sub-Category performance
- Salesperson performance & return behaviour
- Monthly Sales vs Monthly Profit
- Returned orders by Category

### **Why many pivots?**
- Each visualization requires its own pivot for clean formatting.
- Hidden duplicate pivots ensure independent updates without affecting other charts.
- GETPIVOTDATA links ensure the KPI cards remain dynamic.

---

## 3️ Visualizations Built

### **A. Monthly Sales vs Profit Trend (Combo Chart)**
- Line + Column combo
- Shows seasonality, growth, and monthly volatility
- Filtered by Year using slicers

### **B. Salesperson Performance Chart**
- Horizontal bars showing revenue & profit
- Return rate overlay for comparison
- Supports Salesperson slicer interaction

### **C. Segment-wise Analysis Chart**
- Bar chart comparing Consumer, Corporate, and Home Office segments
- Shows profit contribution patterns

### **D. Profit Margin Trend by Segment**
- 100% stacked bar chart
- Tracks margin performance from 2018 to 2021

### **E. Category Profit Margin Donut**
- Shows contribution of Technology, Office Supplies, and Furniture

### **F. Return Analysis (Bar + Donut Combo)**
- Visualizes returned orders and return rates by category  


---

## 4️ Interactive Components

### **Slicers Added**
- **Year**
- **Region**
- **Segment**
- **Salesperson**

### **How slicers work**
- Connected to all PivotTables using PivotTable Connections
- Filtering updates KPIs, charts, and margins simultaneously  
- Duplicate pivots prevent one chart from forcing unwanted changes on another  
- Ensures smooth, real-time interactivity

---

## 5️ Dashboard Layout Strategy

The dashboard is divided into **three structured sections**:

---

### 🔹 **A. KPI Header Section**
- Contains 8 KPIs in grid-aligned format  
- Uses GETPIVOTDATA formulas for real-time dynamic values  
- Conditional formatting highlights negative margins or high return rates

---

### 🔹 **B. Analytical Charts Section**
Contains all major charts:

1. Monthly Sales vs Profit
2. Segment-wise analysis  
3. Salesperson performance  
4. Profit margin trend  
5. Category contribution  
6. Return analysis  

Charts use:
- Consistent color theme  
- Clear labeling  
- Professional spacing  
- No gridline clutter  

---

### 🔹 **C. Interactivity & Filters**
- Slicer panel positioned for easy access  
- Consistent theme applied across slicers  
- Ensures seamless filtering across years/segments/regions


---

## 6️ Dashboard Integration & Final Checks

Before finalizing:
- Verified all slicers refresh correctly  
- Ensured pivot connections were stable  
- Checked that KPI totals match underlying PivotTables  
- Confirmed no blank or error categories appear  
- Optimized layout for executive readability  

---

## ✔️ Summary

This dashboard was built using:
- Advanced pivot modelling  
- KPI engineering  
- Clean, structured visual design  
- Slicer-based interactivity  
- Business-first analytical storytelling  

The result is a fully functional, executive-grade Excel dashboard that transforms raw data into meaningful, actionable insights.

