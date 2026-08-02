# sql_data_analytics_project

This project explores a sales dataset using pure SQL, moving from exploratory data analysis to advanced analytics. It picks up where the [Data Warehouse project](https://github.com/aditi593/SQL_Datawarehouse-project) leaves off, using the Gold layer star schema as the analytical base to answer real business questions.

---

## Project Overview

This project involves:

1. **Exploratory Data Analysis (EDA)**: Understanding the dataset's structure, dimensions, date ranges, and key measures before diving into deeper analysis.
2. **Advanced Analytics**: Using SQL techniques such as window functions and CASE statements to uncover trends, rankings, performance shifts, and segments within the data.
3. **Reporting**: Consolidating the analysis into SQL based reports that summarize customer behavior, product performance, and sales trends.

---

## Part 1: Exploratory Data Analysis (EDA)

Goal: understand the data before analyzing it.

| Step | Focus | Example |
|---|---|---|
| Database Exploration | Explore tables, columns, and schema structure | Reviewing INFORMATION_SCHEMA for available objects |
| Dimensions Exploration | Identify distinct categorical values | `DISTINCT` country, category, product |
| Date Exploration | Understand the time range of the data | `MIN`/`MAX` order date, `DATEDIFF` for span in years |
| Measures Exploration | Identify key numeric values worth aggregating | `SUM(sales)`, `AVG(price)`, `SUM(quantity)` |
| Magnitude Analysis | Compare a measure across a dimension | Total sales by country, total quantity by category |
| Ranking Analysis | Identify top and bottom performers | Top 5 products by revenue, bottom 5 customers by orders |

---

## Part 2: Advanced Analytics

Goal: answer business questions using more advanced SQL techniques.

| Step | Focus | Example |
|---|---|---|
| Change Over Time (Trends) | Track a measure across a date dimension | Total sales by year and month |
| Cumulative Analysis | Track running totals and moving averages | Running total of sales by year using window functions |
| Performance Analysis | Compare current performance to a target or baseline | Current sales vs average sales, current year vs previous year |
| Part-to-Whole (Proportional) Analysis | Understand each category's contribution to the total | Percentage of total sales by product category |
| Data Segmentation | Group records into meaningful buckets | Customers segmented by spend, products segmented by sales range using `CASE WHEN` |
| Reporting | Package analysis into consolidated, reusable views | Customer report, product report combining multiple metrics |

---

## Repository Structure

```
sql-data-analytics-project/
│
├── datasets/                     # Gold layer CSV files used for analysis
│
├── scripts/
│   ├── 00_init_database.sql      # Database and schema setup
│   ├── 01_eda/                   # Exploratory data analysis scripts
│   │   ├── database_exploration.sql
│   │   ├── dimensions_exploration.sql
│   │   ├── date_exploration.sql
│   │   ├── measures_exploration.sql
│   │   ├── magnitude_analysis.sql
│   │   └── ranking_analysis.sql
│   │
│   ├── 02_advanced_analytics/    # Advanced analytics scripts
│   │   ├── change_over_time.sql
│   │   ├── cumulative_analysis.sql
│   │   ├── performance_analysis.sql
│   │   ├── part_to_whole_analysis.sql
│   │   └── data_segmentation.sql
│   │
│   └── 03_reports/               # Final SQL based reports
│       ├── customer_report.sql
│       └── product_report.sql
│
├── README.md                     # Project overview and instructions
└── LICENSE                       # License information for the repository
```

---

## Tools Used

- **SQL Server / SSMS**: Writing and running all analytical queries
- **Gold Layer Star Schema**: Analytical base built in the companion Data Warehouse project
- **Window Functions, CTEs, and CASE Statements**: Core techniques used throughout the advanced analytics section

---

## About This Project

This project was built to apply SQL analytics concepts end to end, from understanding a raw dataset to producing reports that could support real business decisions around customer behavior, product performance, and sales trends. It pairs with the [Data Warehouse project](https://github.com/aditi593/SQL_Datawarehouse-project), which builds the underlying warehouse this analysis runs on.

Course reference: this project was built while following Baraa Khatib Salkini's free SQL course, *Data with Baraa*, on YouTube.
