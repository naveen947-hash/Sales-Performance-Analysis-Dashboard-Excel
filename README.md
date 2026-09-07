# Naveen Excel Mini Project — Sales Performance Analysi Dashboard

## Overview
This workbook is an end-to-end Excel analytics project built on a synthetic **Sales Performance Analysi Dashboard** (500 orders). It takes raw transactional data and turns it into pivot-table summaries and an interactive dashboard with slicers and a timeline filter.

## File
`Naveen_Excel_min_project_.xlsx`

## Sheets

| Sheet | Purpose |
|---|---|
| **Raw data** | The core dataset — 500 orders × 26 columns (customer, order, product, pricing, delivery, and discount details). This is the single source of truth for all analysis. |
| **second data** | A duplicate/working copy of the raw data (used as a secondary source or backup for pivot tables). |
| **Sheet1** | Pivot tables summarizing metrics such as max delivery-inclusive amount by customer and count of products ordered. |
| **Sheet3** | Additional pivot tables — average customer age, sum of order amount, sum of amount by customer, count of orders — filtered by a Coupon Code slicer. |
| **dashborad** | The main interactive dashboard sheet, built from 10+ charts (bar/column/line/pie-style visuals) plus slicers and a timeline. |

## Data Dictionary (Raw data / second data)
| Column | Description |
|---|---|
| Customer_ID, First_Name, Last_Name, Full_Name | Customer identity |
| Age, Gender, City, Email, Address | Customer demographics/contact |
| Order_ID, Order_Date, Order_Time | Order identifiers and timing |
| Product_ID, Price, Quantity | Product and line-item pricing |
| Coupon_Code | Discount coupon applied (e.g., FLAT8) |
| Estimated_Days_to_Deliver, Delivery_Charge, Delivery_Date, Delivery_Time | Delivery logistics |
| Day_Delivery | Delivery day count/flag |
| Amount | Order value before delivery charge |
| Discount_Percentage, Discount_Amount | Discount applied |
| Amount_with_Delivery_Charge | Final payable amount |
| Delivery_Status | e.g., BeforeTime / OnTime / Delayed |
| Order month | Month number extracted from Order_Date |

## Dashboard Features
<img width="1677" height="792" alt="image" src="https://github.com/user-attachments/assets/8748ebfc-2310-4758-8318-b3f806388a52" />

- **Charts**: Multiple pivot charts (10 charts + 2 extended charts) visualizing sales, delivery, and customer metrics.
- **Slicers**: City, Coupon_Code, Gender, Product_ID — for interactive filtering.
- **Timeline**: Order_Date native timeline control for filtering by date range.
- **Pivot Tables**: Summaries by customer, product, and coupon (sum/average/count/max of key metrics).

## How to Use
1. Open the workbook in Excel (slicers/timelines require Excel 2013+; some features use Excel 365 dynamic arrays/spill functions).
2. Go to the **dashborad** sheet to explore the interactive view.
3. Use the slicers (City, Coupon Code, Gender, Product) and the Order Date timeline to filter all connected charts and pivots simultaneously.
4. Refer to **Sheet1** and **Sheet3** for the underlying pivot table logic behind the dashboard visuals.
5. **Raw data** / **second data** contain the source records — refresh pivot tables (Data → Refresh All) if the raw data is edited.

## Notes
- "second data" appears to be a working duplicate of "Raw data," likely used to avoid disturbing the original source while building extra pivots.
- Column header `Amount_with_Delivery_Charge ` contains a trailing space in the original file — keep this in mind if referencing it in formulas.
