Home Sales Data Analysis with PySpark
Overview
This project analyzes home sales data using PySpark. The dataset, home_sales_revised.csv, is loaded from an AWS S3 bucket into a PySpark DataFrame. Various SQL queries are executed to explore home prices based on different attributes. The performance of these queries is optimized using caching and partitioning techniques.
Steps
File Setup
•	Rename Home_Sales_starter_code.ipynb to Home_Sales.ipynb.
Data Import and Table Creation
•	Import necessary PySpark SQL functions.
•	Load home_sales_revised.csv from the AWS S3 bucket into a PySpark DataFrame.
•	Create a temporary table named home_sales for SQL-based analysis.
Data Analysis
The following analyses are conducted using SparkSQL:
1.	Average Price of Four-Bedroom Homes Sold Per Year
o	Determine the average price for four-bedroom homes sold each year.
o	Results are rounded to two decimal places.
2.	Average Price of Three-Bedroom, Three-Bathroom Homes by Year Built
o	Identify the average price for homes with three bedrooms and three bathrooms for each year they were built.
3.	Average Price of Homes with Specific Features
o	Focus on homes that have three bedrooms, three bathrooms, two floors, and a living space of at least 2,000 square feet.
o	Find the average price for each year these homes were built.
4.	Average Home Price by "View" Rating (Above $350,000)
o	Identify average home prices per "view" rating where the average price is at least $350,000.
o	Measure the runtime of this query.
Performance Optimization
•	Cache the home_sales Table: Improves query performance by storing data in memory.
•	Verify Caching: Ensure the table is cached using PySpark's catalog functions.
•	Compare Cached vs. Uncached Query Performance: Measure the runtime difference when using cached data.
•	Partition Data by date_built: Organize data into partitions to enhance query efficiency.
•	Save Data as Parquet Format: Store partitioned data in Parquet format for better performance.
•	Compare Partitioned vs. Uncached Query Performance: Run queries on partitioned data and analyze performance improvements.
Cleanup
•	Uncache home_sales Table: Free up memory by removing the cached table.
•	Verify Uncaching: Check that the table is no longer cached in PySpark.
Conclusion
This project demonstrates how to use PySpark for large-scale data analysis, optimize performance using caching and partitioning, and efficiently query structured data using SparkSQL.

# Home_Sales
