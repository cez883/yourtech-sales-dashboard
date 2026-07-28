# Sales Analytics Dashboard for a Multi-Channel Electronics Retailer (Power BI)

## Executive Summary

The project presents a six-page Power BI dashboard developed for **YourTech.com**, a fictional multi-channel electronics retailer. The report provides a single source of truth for analysing sales performance, marketing campaigns, customer behaviour, and product profitability.

The dashboard enables users to move from high-level KPIs to detailed customer-level analysis through interactive filtering and drillthrough functionality.

<img width="1952" height="1096" alt="image" src="https://github.com/user-attachments/assets/7e2593b9-83fb-4d09-8611-558ab6b18132" />

## Business Problem

Different business departments relied on separate spreadsheet exports and manual reporting, resulting in inconsistent answers to the same business questions.

The objective was to build a single interactive report capable of answering key business questions for Sales, Marketing, Product Management, and Customer Support teams.

<img width="1951" height="1094" alt="image" src="https://github.com/user-attachments/assets/e5466e5d-fb12-4bbb-890e-f40c065142aa" />

## Dashboard Pages

## 1. Sales Performance
Provides an executive overview of overall business performance including:
- KPI summary
- Monthly sales trend
- Sales by channel
- Sales by category
- Year-over-Year growth by category
- Sales by promotional event

## 2. Campaign Performance
Analyses promotional effectiveness through:
- Campaign revenue contribution
- Campaign sales and orders
- Campaign profitability
- Average discount
- Revenue comparison by campaign and year
- Sales channel distribution by campaign

## 3. Customer Insights
Explores customer behaviour by analysing:
- Customer demographics
- Revenue by age group
- Average order value
- Revenue by gender
- Product preferences by age group
- Returning Customer Rate
- Top customers

## 4. Product & Brand Insights
Evaluates commercial performance of products and brands:
- Top products
- Brand performance
- Revenue and Gross Profit by category
- Gross Margin comparison
- Category performance matrix

## 5. Customer Order Details (Drillthrough)
Provides customer-level analysis including:
- Customer profile
- Customer Since
- Lifetime Sales
- Average Order Value
- Total Orders
- Favourite Category
- Complete purchase history

## 6. Business Questions
Navigation page linking business questions to the relevant report pages.


## Methodology

1. For the purpose of this project I have created a dataset containing three .csv files: Customers, Sale_Event as well as YourTech_Orders containing over 100k rows of sale transactions data.
2. Imported and transformed raw sales data using Power Query.
3. Designed a star-schema semantic model consisting of one fact table and six dimension tables.
4. Created reusable DAX measures for sales, profitability, campaign analysis, customer metrics, and time intelligence (YoY, YTD).
5. Designed six report pages, each focused on a specific business area.
6. Implemented drillthrough functionality for customer-level analysis.
7. Applied consistent navigation, slicers and conditional formatting across the report.

## Skills

**Power Query:** ETL, data cleaning, locale-aware date parsing
**DAX:** CALCULATE, FILTER, TOPN, MAXX, SUMX, DISTINCTCOUNT, COUNTROWS, time intelligence
**Data Modelling:** star-schema, dimension modelling, date table design, 

## Data Model

The report is built using a **Star Schema** consisting of:

**Fact Table**
- fSales

**Dimension Tables**
- dCustomers
- dProducts
- dDate
- dStores
- dStaff
- dSale Event

This structure improves performance and follows Power BI modelling best practices.

<img width="1746" height="1158" alt="image" src="https://github.com/user-attachments/assets/1d7ac81b-7bd4-4788-a6f7-af027b38ee11" />

## Key Insights

The dashboard enables business users to:

- Monitor overall sales performance through KPI tracking and Year-over-Year growth analysis.
- Identify which sales channels, product categories and brands generate the highest revenue and profit.
- Evaluate the effectiveness of promotional campaigns including Black Friday, Summer Sale and Boxing Day.
- Analyse customer demographics, purchasing behaviour and repeat customer rates.
- Review complete customer purchase history and lifetime value through drillthrough functionality.

## Next Steps

1. Add row-level security so store managers only see their own store's data.
2. Enhance customer retention analysis with cohort and repeat purchase trends.

---
*Built on a synthetic dataset designed to resemble a real multi-channel electronics retailer, for portfolio purposes only.*
