# Home_Sales
Module 22 Homework

## Home Sales Analysis with PySpark

### Overview

This project analyzes a home sales dataset using Pyspark to uncover trends in housing prices based on various attributes. The analysis includes creating temporary tables, preforming SQL queries, caching and uncaching tables, and optimizing performance with Parquet partitioning. The dataset was sourced form provided AWS S3 link, and all queries wer executed using PySpark SQL.

### Tools and Technologies

* PySpark: Distributed data processing and SQL querying
* Python; Data analysis and scripting
* AWS S3: Data storage (source file)
* GitHub: version control and project repository

### Dataset

The dataset (home_sales_revised.csv) includes the following fields

* id: Unique identifiers for each home sale
* date: Data the home was sold
* date biult: Year the home was built
* price: Sale price of the home
* bedrooms: Number of bedrooms
* bathrooms: Number of bathrooms
* sqft_living: Square footage of the living area
* sqft_lot: Lot size in square feet
* floors: Numer of floors
* waterfront: Waterfront property indicator (1= Yes, 0= No)
* view: Quatlity of the view (0-100 scale)

### Key Analyses Performed

1. Average Price of 4-Bedroom Homes Sold by Year
2. Average Price of 3-Bedroom, 3-Bathroom Homes by Year Built
3. Average Price of 3-Bedroom, 3-Bathroom, 2-Floor Homes ≥ 2000 sqft by Year Built
4. Average Price per Viewing Rate (with Avg Price ≥ $350,000)
5. Performance Comparison: Uncached vs. cached Queries
6. Partitioned Data by date_built and Performance Comparison on Parquet Data

### Project Highlights

* Temporary View: Created for SQL querying on the DataFrame.
* Caching: Improve query preformance by cahing home_sales table.
* Partitioning: Optimized data storage by partitioning on date_built.
* Preformance Analysis: Measured query runtimes for uncached, cached, and partitioned data.
* SQL Queries: Used PySpark SQL for complex data filtering, grouping, and aggregation.

### Results Summary

| Query Description                        | Runtime (Uncached)                   | Runtime (Cached)              | Runtime (Partitioned Parquet) |
| ---------------------------------------- | ------------------                   | ----------------              | ----------------------------- |
| Average Price per View Rating (≥ \$350K) | 0.16480493545532227 seconds          | 0.3188474178314209 seconds    | 0.259918212890625 seconds     |                      |


### How to Run

1. Clone this repository:

```git clone https://https://github.com/JenniBean-K/Home_Sales```

2. Open `Home_Sales.ipynb` in Jupyter.

3. Follow the cells to run the analysis end-to-end.



