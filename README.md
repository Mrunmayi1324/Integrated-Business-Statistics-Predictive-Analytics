# Integrated Business Statistics & Predictive Analytics

## Project Overview

This project analyzes retail transaction data to uncover sales trends, understand customer purchasing behavior, and support data-driven business decisions. It combines statistical analysis, hypothesis testing, regression modeling, sales forecasting, SQL queries, and Excel reporting in a single analytical workflow.

The project uses the **Online Retail dataset from the UCI Machine Learning Repository** and Python-based analytical tools to transform raw transactional data into meaningful business insights.

## Business Objectives

- Analyze sales revenue, order volume, and customer purchasing patterns.
- Identify top-performing products and countries.
- Apply descriptive and inferential statistics to understand business performance.
- Examine relationships between customer spending and purchasing frequency.
- Demonstrate A/B testing concepts using a simulated experiment.
- Forecast short-term sales revenue using time-series analysis.
- Perform SQL-based business reporting.
- Prepare an Excel workbook for presenting analytical results.

## Dataset

**Source:** UCI Machine Learning Repository — Online Retail

**Link:** https://archive.ics.uci.edu/dataset/352/online+retail

The dataset contains transactional records from a UK-based online retailer.

Key attributes include:

| Column | Description |
|---|---|
| InvoiceNo | Invoice or transaction identifier |
| StockCode | Product code |
| Description | Product description |
| Quantity | Number of units purchased |
| InvoiceDate | Date and time of transaction |
| UnitPrice | Price per unit in pounds sterling |
| CustomerID | Customer identifier |
| Country | Customer's country |

## Technologies Used

- **Python:** Data analysis and statistical computing
- **Pandas & NumPy:** Data manipulation and numerical calculations
- **Matplotlib & Seaborn:** Data visualization
- **SciPy:** Statistical hypothesis testing
- **Statsmodels:** Regression modeling and time-series forecasting
- **SQLite:** SQL-based business analysis
- **Excel / OpenPyXL:** Reporting and spreadsheet preparation
- **Jupyter Notebook:** Development and analysis environment

## Project Workflow

### 1. Data Cleaning and Preparation
- Identified duplicate records and missing values.
- Excluded cancellation invoices and transactions with non-positive quantities or unit prices.
- Converted transaction dates to datetime format.
- Calculated transaction-line revenue using quantity multiplied by unit price.

### 2. Exploratory Data Analysis
- Calculated total revenue, order volume, units sold, and average order value.
- Analyzed revenue distributions.
- Identified top products and countries by revenue.
- Examined monthly sales trends.

### 3. Statistical Analysis
- Calculated descriptive statistics and confidence intervals.
- Applied Welch's t-test to compare customer spending between selected countries.
- Used chi-square testing to examine the association between country and repeat-customer status.
- Used Spearman correlation to investigate the relationship between order frequency and total customer spending.

### 4. Regression Analysis
- Applied linear regression to examine customer spending in relation to order frequency and country.
- Applied logistic regression to examine associations between country and repeat-customer status.
- Evaluated model coefficients, p-values, odds ratios, and regression diagnostics.

### 5. A/B Testing
- Created a simulated control and treatment experiment.
- Compared conversion rates using a chi-square test.
- Calculated absolute and relative conversion-rate lift.
- Examined statistical significance and confidence intervals.

*Note: The A/B test uses simulated data and does not represent an actual experiment conducted on the retailer's customers.*

### 6. Sales Forecasting
- Aggregated transaction revenue into monthly totals.
- Applied Holt's exponential smoothing model to demonstrate short-term forecasting.
- Visualized historical revenue and forecast values.

*Note: The original dataset covers approximately one year. Forecasts are exploratory and have limitations in capturing annual seasonality.*

### 7. SQL Business Analysis
- Created a local SQLite database.
- Used SQL aggregation and filtering to analyze revenue, orders, products, countries, and customers.
- Generated monthly revenue summaries.

### 8. Excel Reporting
- Consolidated business KPIs, monthly sales, top products, country performance, A/B testing results, and forecasts into an Excel workbook.

## Key Deliverables

- `cleaned_online_retail.csv` — Cleaned transaction data
- `descriptive_statistics.csv` — Descriptive statistics
- `business_kpis.csv` — Key business metrics
- `top_10_products.csv` — Highest-revenue products
- `top_10_countries.csv` — Country performance summary
- `customer_level_analysis.csv` — Customer-level analysis
- `linear_regression_results.csv` — Linear regression results
- `logistic_regression_results.csv` — Logistic regression results
- `ab_testing_summary.csv` — Simulated experiment summary
- `ab_testing_results.csv` — A/B test statistics
- `monthly_sales.csv` — Monthly revenue data
- `sales_forecast.csv` — Forecasted revenue
- `online_retail_analysis.db` — SQLite database
- `Statistical_Analysis_Report.xlsx` — Consolidated Excel report

*Some files are generated only after the corresponding notebook sections have been executed successfully.*

## Business Value

This project demonstrates how statistical techniques and analytical tools can support retail decision-making. The workflow helps organize sales performance information, investigate customer behavior, compare business segments, and demonstrate forecasting and experimentation methods.

The results can inform further investigation into product performance, customer engagement, and sales planning. Statistical associations should not be interpreted as causal relationships without additional evidence.

## Limitations

- The analysis uses historical transaction data from a limited period.
- Some customer identifiers are missing, restricting customer-level analysis.
- Cancelled invoices and non-positive transaction lines are excluded from the primary sales analysis.
- The A/B testing results are simulated.
- Forecast reliability is limited by the short historical period.
- Regression findings describe associations and depend on model assumptions.

## How to Run the Project

1. Download the Online Retail dataset from the UCI repository.
2. Install Python and Jupyter Notebook.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels openpyxl
   ```

4. Place `Online Retail.xlsx` in your project directory or update the dataset path in the notebook.
5. Execute the notebook cells in order, from data loading through Excel reporting.
6. Review the generated CSV files, SQLite database, charts, and Excel workbook.

## Conclusion

The Integrated Business Statistics & Predictive Analytics project demonstrates an end-to-end analytical workflow, from data preparation and statistical investigation to regression, forecasting, SQL analysis, and business reporting.

It provides practical experience relevant to entry-level Statistical Analyst, Data Analyst, and Business Analytics roles.

## Dataset Citation

Chen, D. (2015). *Online Retail*. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33
