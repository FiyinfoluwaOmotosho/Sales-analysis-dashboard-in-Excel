# Sales-analysis-dashboard-in-Excel
An Excel-only sales analysis project. It takes 1,000 sales transactions from 2023, summarises them with seven pivot tables, and presents the results in an interactive dashboard with four KPI cards, seven charts and three slicers. No code or outside tools were used for the dashboard.

Sales analysis dashboard
# Business problem
A sales team of five reps sells four product categories across four regions, online and in stores. Management has transaction-level data but no single view of how the business is doing. The dashboard gives that view, and the analysis behind it looks at where the money comes from, where it is lost, and what the team could do differently.

The project answers these questions:

- How much revenue and gross profit did the business make, and how many units were sold?
Which sales reps, regions and product categories brought in the most?
- How did sales change from month to month?
- How do customers pay, and do new and returning customers differ?
- How large are the discounts, and what do they do to profit?

# Dataset
This dataset was gotten from Kaggle
[Download here](https://www.kaggle.com/).
The data was formatted as an Excel Table named SalesData. It has 1,000 rows and 14 columns. Sale dates run from 1 January 2023 to 1 January 2024. 997 rows fall in 2023 and 3 are dated 1 January 2024.

## Dataset Preview
<img width="1920" height="1080" alt="Screenshot 2026-11-18 014104" src="https://github.com/user-attachments/assets/6e119e08-38d9-46e5-9d77-616c313be3b5" />

# Data preparation
- Converted the range to an Excel Table (Table1) so formulas and pivot tables read from one named source and pick up new rows.
- Checked every column for blanks and the whole table for duplicate rows. None were found.
- Checked that Revenue equals Quantity_Sold x Unit_Price on every row.
- Grouped Sale_Date by month and year inside the pivot table to get the monthly trend.
- Built the pivot tables from Table1 on a separate Tables sheet, then linked the charts to them.

# KPIs (Key Performance Indicator) 
- Total revenue	$70,329,941: Sum of Revenue, taken from the pivot table grand total
- Total units sold	25,355:	Sum of Quantity_Sold, taken from the pivot table grand total
- Gross profit	$6,487,847	=SUMPRODUCT(Table1[Quantity_Sold],Table1[Unit_Price])-SUMPRODUCT(Table1[Quantity_Sold],Table1[Unit_Cost])
- Average discount	15%	=AVERAGE(Table1[Discount]) (15.24% before rounding)
  
Gross profit here is 9.2% of revenue. It is worked out at list price, before any discount is taken off. The profitability section below shows what happens once discounts are included

# Pivot Tables
The analysis sits on the Tables sheet. It has seven pivot tables, all built from SalesData, and each one feeds one chart on the dashboard. Each pivot table groups the 1,000 transactions by one field, such as sales rep, region or month, and totals, counts or averages one measure for each group. Changing a slicer on the dashboard filters the pivot tables, and the charts update with them
## PivotTable Preview
<img width="1420" height="625" alt="Screenshot 2026-11-18 014018" src="https://github.com/user-attachments/assets/5441420e-f716-45cb-b3a6-c6d5a2ea13ad" />

# Dashboard
The left panel holds the logo, three navigation buttons (Dashboard, Analysis, Database) and slicers for Product_Category, Region and Sales_Rep. The header sits at the top, with the four KPI cards underneath and the seven charts below them. The layout is built from rounded rectangles, icons and text boxes placed over the Dashboard sheet, with a blue and black colour scheme
## Dashboard Preview
<img width="1553" height="747" alt="Screenshot 2026-11-18 014719" src="https://github.com/user-attachments/assets/96854701-6711-4141-aa68-29c9ae42d81f" />
