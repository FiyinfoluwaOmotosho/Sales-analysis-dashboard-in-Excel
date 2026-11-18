# Sales Performance Analysis Dashboard in Excel
An Excel only sales analysis project. It takes 1,000 sales transactions from 2023, summarizes them with seven pivot tables, and presents the results in an interactive dashboard with four KPI cards, seven charts and three slicers. No code or outside tools were used for the dashboard.
[Download Dataset](https://github.com/user-attachments/files/35037018/sales_data.csv) .

Sales analysis dashboard
# Business problem
A sales team of five reps sells four product categories across four regions, online and in stores. Management has transaction-level data but no single view of how the business is doing. The dashboard gives that view, and the analysis behind it looks at where the money comes from, where it is lost, and what the team could do differently.

The project answers these questions:

- How much revenue and gross profit did the business make, and how many units were sold?
- Which sales reps, regions and product categories brought in the most?
- How did sales change from month to month?
- How do customers pay, and do new and returning customers differ?
- How large are the discounts, and what do they do to profit?

# Database
This dataset was gotten from Kaggle
[Download here](https://www.kaggle.com/) .
The data was formatted as an Excel Table named SalesData. It has 1,000 rows and 14 columns. Sale dates run from 1 January 2023 to 1 January 2024. 997 rows fall in 2023 and 3 are dated 1 January 2024.

## Dataset Preview
<img width="1920" height="1080" alt="Screenshot 2026-11-18 014104" src="https://github.com/user-attachments/assets/6e119e08-38d9-46e5-9d77-616c313be3b5" />

# Data preparation
- Converted the range to an Excel Table (SalesData) so formulas and pivot tables read from one named source and pick up new rows.
- Checked every column for blanks and the whole table for duplicate rows. None were found.
- Checked that Revenue equals Quantity_Sold x Unit_Price on every row.
- Grouped Sale_Date by month and year inside the pivot table to get the monthly trend.
- Built the pivot tables from (SalesData) on a separate Tables sheet, then linked the charts to them.

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

# Key Insights
## Sales performance
- Revenue was $70.33 million on 25,355 units. The average transaction was worth $70,330 and covered about 25 units.
- David led all reps with $16.40 million, about 23% of total revenue. Eve followed with $15.27 million, Bob and Alice sat close together at $13.71 million and $13.40 million, and Charlie was lowest at $11.55 million. Charlie also closed the fewest deals (169, against 192 to 222 for the others).
- The reps have different strengths. Eve's best category is Clothing ($4.88 million), David's is Electronics ($4.80 million) and Bob's is Furniture ($4.36 million). Charlie's weakest are Food ($2.42 million) and Furniture ($2.47 million).
- North sold the most units (6,705) and South the fewest (5,808). By revenue the regions are closer: North $18.21 million, East $18.08 million, West $17.76 million, South $16.28 million.
- Clothing brought in the most revenue ($19.29 million), then Furniture ($18.33 million), Electronics ($17.57 million) and Food ($15.14 million). Food is the weakest category and trails in every region except South.
- The top 100 transactions (10%) make up 27% of revenue, so sales are not dependent on a few large orders.

# Recommendations
- Limit discounts to 10% unless a manager approves a higher rate. The data shows 10% is roughly the point where a sale stops making money, and nothing in the volumes suggests the deeper discounts are buying extra sales.
- Review pricing. A markup of about 10% leaves very little room. Options are raising list prices, renegotiating unit costs with suppliers, or both, starting with the categories with the weakest margin after discounts (Furniture and Clothing).
- Judge reps on profit as well as revenue. David and Eve bring in the most revenue, and they also have the highest average discounts (16.5% and 15.8%). Share the discount data with each rep and set a target for the share of deals above 20% off, which is 40% for David, 36% for Charlie and 34% for Eve.
- Move reps toward their strengths. Eve in Clothing, David in Electronics and Bob in Furniture each bring in $4.3 million or more in one category. Charlie's weakest categories (Food and Furniture) are a place for coaching or a change of account mix.
- Support Food and the South region. Food has the lowest revenue of the four categories, and South has the lowest revenue of the four regions. Look at stock, pricing and local demand before adding more sales effort.
- Plan for the slow months. July, September and November are the weakest, and Q3 is the weakest quarter. Use bundles, loyalty offers or payment terms in those months in place of price cuts, since price cuts lose money on this data.
- Update the dashboard. Add net revenue and net profit KPI cards, and correct the chart titles listed in the notes below, so the dashboard does not show a profit the business is not making.

  # Conclusion
The dashboard shows a business with steady sales spread fairly evenly across reps, regions, categories and channels. The weak point is pricing. With a markup near 10% and an average discount of 15%, most deals are sold below cost, and the $6.49 million gross profit on the dashboard turns into a loss of about $4.16 million once discounts are counted. Controlling discounts is the clearest way to improve results, and it can be done without changing the sales team or the product range
