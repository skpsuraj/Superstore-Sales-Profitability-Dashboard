# Superstore Sales & Profitability Dashboard
A 2-page Power BI dashboard built on the Superstore retail dataset (9,994 orders, 2011–2014). 
Data was cleaned and feature-engineered in Python before being loaded into Power BI.

## What it does
Page 1 gives an overview of sales, profit, and regional performance. Page 2 digs into why 
certain products and states aren't profitable — mainly driven by high discounting. There's 
also a drill-through page: clicking any state on the map/chart opens a dedicated breakdown 
showing which categories, discount bands, and products are responsible for that state's 
performance.

## Key findings
- Orders with 40%+ discount lost the company roughly $99,500 overall — discounting past 
  20% consistently erodes margin regardless of category.
- Tables and Bookcases are the only two sub-categories that lose money overall, despite 
  reasonable sales volume.
- States like Texas, Ohio, and Illinois rank in the top 10 by sales but are net-negative 
  on profit — high volume doesn't mean high margin here.

## How it was built
1. **Python (pandas)** — data validation, type fixes (dates, postal codes), and feature 
   engineering: profit margin, shipping days, discount bands, year/quarter/month splits.
2. **Power BI** — DAX measures for dynamic KPIs (e.g., worst/best performing sub-category 
   updates automatically with filters), conditional formatting to flag loss-making 
   categories, and a drill-through page for state-level root cause analysis.

## Files
- `data_cleaning.py` — cleaning and feature engineering script
- `Superstore_Cleaned.csv` — output dataset used in Power BI
- `Superstore_Sales_Dashboard.pbix` — the dashboard file
- Screenshots below

## Screenshots
![Sales Overview](
<img width="1277" height="716" alt="Dashboard_view_1" src="https://github.com/user-attachments/assets/866e355b-3cca-45f9-a19c-dc420268aea1" />
)
![Product & Discount Analysis](
<img width="1277" height="717" alt="Dashboard_view_2" src="https://github.com/user-attachments/assets/e0e6d9d3-6bf0-4870-8ca3-a172a616d159" />

)
