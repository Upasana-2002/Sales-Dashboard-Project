# Sales Dashboard Project

## Project Overview
This Power BI dashboard provides a comprehensive analysis of sales data for a company. It visualizes key metrics, trends, and insights to support data-driven decision-making. The dashboard is interactive and allows exploration by product, customer, and geography.

---

## Dataset
- File: `sales_data_sample.csv`
- Description: Contains transactional sales data with the following columns:
---

## Dashboard Pages
1. **Home** – KPI cards (Total Sales, Sales Growth %, Profit %), Sales Trend, Product Line, Deal Size, Top Territories  
2. **Customer** – Customer sales analysis, top customers, deal sizes  
3. **Product** – Product performance, quantity, and sales distribution  
4. **Global** – Map & bar charts for sales by country, state, and city  

---

## Key Measures

- **Total Sales:** `SUM('sales_data_sample'[SALES])`  
- **Previous Year Sales:** `CALCULATE([Total Sales], SAMEPERIODLASTYEAR('sales_data_sample'[ORDERDATE]))`  
- **Sales Growth %:** `DIVIDE([Total Sales] - [Previous Year Sales], [Previous Year Sales], 0)`  
- **Profit %:** `DIVIDE([Total Sales] - SUMX('sales_data_sample', 'sales_data_sample'[MSRP] * 'sales_data_sample'[QUANTITYORDERED]), [Total Sales], 0)`

---

## Usage
Open `SalesDashboard.pbix` in Power BI Desktop and interact with slicers to explore sales by product, customer, or territory.


---


