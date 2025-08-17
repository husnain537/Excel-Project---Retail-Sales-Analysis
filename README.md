# Excel-Project Retail-Sales-Analysis
You are a Data Analyst at an e-commerce company aiming to enhance sales strategies and customer satisfaction. Your objective is to analyze online retail transaction data to uncover insights into sales performance, customer behaviour, and product trends.

Dataset Description:

- Invoice No: Unique identifier for each transaction
- Stock Code: Product/item code
- Description: Product description
- Quantity: Number of items purchased
- Invoice Date: Date and time of transaction
- Unit Price: Price per unit in GBP
- Customer: Unique identifier for each customer
- Country: Country of the customer

Objectives:

Clean and prepare retail sales data in Excel by fixing errors, creating new features, and organizing it properly. Analyze sales trends, customer behavior, product performance, and geographical insights through simple calculations and visualizations.
Create a clean, professional dashboard with filters to easily explore and update the sales data.

Data Cleaning Steps:

1 Customer ID Column: Handled blank values in the Customer ID column. If the analysis focuses on customers, blank values must be removed. If the focus is on products or inventory, keeping or removing them is optional unless they cause issues during analysis.

2	Invoice No column: 2nd thing is that in invoice no column some values were numeric, and some were like alphabet at the start (C) so i flag them as deliver order & Cancel order.


3	Stock code column: Removed text values (e.g., Post, D, M) from Stock Code column because their descriptions were unclear and did not correspond to valid products. Since working independently, unable to verify with team; decision made to improve data quality for product sales analysis.

4	Date column: In date column i extract hours, day of the week, Month & Year for better analysis.

5	Quantity Column: Identified and removed 9 extreme outliers (both high positive and high negative values) in the Quantity column. For the remaining values, applied a threshold of 1,500 to flag unusually large transactions and reduce confusion. Created two custom columns: Quantity Status (Sales, Return) to classify transaction type, and Quantity Outlier Flag (Flag, Normal) to indicate whether a value exceeds the threshold.


6	Country Column: I found some "Unspecified" values in the Country column, so I did not impute them with the mode because that would artificially increase the share of a particular country and affect the analysis. My dataset has 400K rows, and the "Unspecified" values total just 244, which is about 0.06%. Therefore, I removed these rows, thinking that this small number would not impact future analysis.

	I created a total of 10 custom columns from the dataset using Excel formulas for better and deeper analysis:

	Order Status
 
	Stock/Product Code Status
 
	Quantity Status
 
	Quantity Outlier Flag
 
	Date Breakdown (Hour, Day of Week, Month, Year)
 
	Total Revenue and Revenue Status

