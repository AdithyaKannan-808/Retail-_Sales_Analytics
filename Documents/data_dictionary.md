#  Data Dictionary

This file defines all columns used in the **Retail Sales Analytics Dashboard (2018–2021)**.

---

##  Field Definitions

| Column Name              | Description                                                   | Data Type        | Example          |
|--------------------------|---------------------------------------------------------------|------------------|------------------|
| Order ID                | Unique identifier for each transaction                        | Text/String      | CA-2021-12345    |
| Order Date              | Date when the order was placed                                | Date             | 2021-07-12       |
| Sales                   | Monetary value of the order                                   | Decimal/Float    | 450.75           |
| Profit                  | Profit earned from the order                                  | Decimal/Float    | 89.20            |
| Quantity (Order Count)  | Number of units sold in the transaction                        | Integer          | 5                |
| Category                | Main product category                                          | Text/String      | Technology       |
| Sub-Category            | Detailed product type within the category                      | Text/String      | Phones           |
| Segment                 | Customer segment (Consumer, Corporate, Home Office)            | Text/String      | Consumer         |
| Region                  | Geographic region of the customer                              | Text/String      | West             |
| Returned Orders         | Whether the order was returned (1 = returned, 0 = not returned) | Integer (0/1)    | 1                |
| Profit Margin %         | Profit ÷ Sales × 100                                           | Calculated Field | 19.4%            |
| Year                    | Extracted year from Order Date                                 | Integer          | 2021             |

---

##  Derived / Calculated Metrics

| Field                  | Definition                                |
|------------------------|---------------------------------------------|
| Profit Margin %        | Profit ÷ Sales × 100                        |
| Return Rate %          | Returned Orders ÷ Total Orders × 100        |
| Avg Profit per Order   | Profit ÷ Order Count                        |
| Buyer Segment Margin   | Average profit margin by customer segment   |
| Region Segment Margin  | Average profit margin by region             |

---

##  Notes

- Some fields (like Profit Margin %) are **not present in raw data** — they are calculated during analysis.  
- Region/Segment performance is aggregated via **PivotTables**.  
- Date components (Year) are extracted for **slicer filtering**.

