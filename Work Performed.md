## Data Cleaning in Power Query

- Imported the three CSV files (customers.csv, orders.csv, products.csv) into Excel Power Query.

- Fixed date columns: Converted Order_Date and Delivery_Date in orders.csv to proper date format (e.g., from text to date type).

- Adjusted column types: Changed Quantity and Price to numbers; ensured Customer_ID and Product_ID were text for consistent joining.

- Removed any duplicates or null values in key columns (e.g., no blank Order_IDs).

- Loaded cleaned data into Excel tables for modeling.

## New Columns Created

- In orders.csv (via Power Query or Excel formulas):

  - **Revenue**: Calculated as Price × Quantity for each order line.

  - **Delivery Days**: Calculated as Delivery_Date - Order_Date (result in days).

  - **Hour**: Extracted the hour from Order_Date (using HOUR function) to analyze order times.

  - **Month**: Extracted the month name from Order_Date (using TEXT function, e.g., "MMMM") for monthly trends.

## Data Modeling

- Used Excel's Data Model to create relationships:

  - Linked orders.csv to customers.csv using Customer_ID (one-to-many).

  - Linked orders.csv to products.csv using Product_ID (one-to-many).

- This allowed pivoting and aggregating data across tables (e.g., revenue by city or category).

## KPIs and Analysis Created

- All analysis done using PivotTables, PivotCharts, and formulas in Excel.

- **Total Revenue**: Sum of Revenue column across all orders (PivotTable grand total).

- **Average Delivery Time**: Average of Delivery Days column (PivotTable average).

- **Monthly Sales Performance**: PivotTable with Month as rows, Sum of Revenue as values; added line chart.

- **Top Products by Revenue**: PivotTable with Product Name as rows, Sum of Revenue as values; filtered to top 5.

- **Average Order Value**: Average of Revenue column per order (PivotTable average).

- **Top Categories by Revenue**: PivotTable with Category as rows, Sum of Revenue as values; added bar chart.

- **Top 10 Cities by Number of Orders**: PivotTable with City as rows, Count of Order ID as values; sorted descending and filtered to top 10; added bar chart.

- **Orders by Hour**: PivotTable with Hour as rows, Count of Order ID as values; sorted by hour; added line chart.

- **Revenue by Occasions**: PivotTable with Occasion as rows, Sum of Revenue as values; added bar chart.

- **Total Orders**: Count of Order ID across all data (PivotTable count).

- Visuals: Used Excel charts (line, bar) inserted next to PivotTables for a simple dashboard view.

This setup created a basic Excel dashboard with tables and charts .