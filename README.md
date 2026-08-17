# Sales Analytics Dashboard for a Multi-Channel Electronics Retailer (Power BI)

## Executive Summary

The project presents a five-page Power BI dashboard developed for **YourTech.com**, a fictional multi-channel electronics retailer. The report provides a single source of truth for analysing sales performance, marketing campaigns, customer behaviour, and product profitability.

The dashboard enables users to move from high-level KPIs to detailed customer-level analysis through interactive filtering and drillthrough functionality.

screenshots/01_sales_performance.png


## Business Problem

The objective was to build a single interactive report capable of answering key business questions for Sales, Marketing, Product Management, and Customer Support teams so the departments don't have to rely on separate spreadsheet exports and manual reporting. 

screenshots/06_business_questions.png

## Dashboard Pages

## 1. Sales Performance  
Executive overview of sales trends, revenue distribution, profitability, and year-over-year growth across products and sales channels:
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

screenshots/04_product_brand_insights.png

## 5. Customer Order Details (Drillthrough)
Provides customer-level analysis including:
- Customer profile
- Customer Since
- Lifetime Sales
- Average Order Value
- Total Orders
- Favourite Category
- Complete purchase history


## Methodology

1. For the purpose of this project I have designed and generated a synthetic retail dataset consisting of over 100k sales transactions together with Customer and Sale Event dimension tables.
2. Imported and transformed raw sales data using Power Query.
3. Designed a star-schema semantic model consisting of one fact table and six dimension tables.
4. Created reusable DAX measures for sales, profitability, campaign analysis, customer metrics, and time intelligence (YoY, YTD).
5. Designed five report pages, each focused on a specific business area.
6. Implemented drillthrough functionality for customer-level analysis.
7. Applied consistent navigation, slicers and conditional formatting across the report.


## Skills

**Power Query:** ETL, data cleaning, locale-aware date parsing  
**DAX:** CALCULATE, FILTER, TOPN, MAXX, SUMX, DISTINCTCOUNT, COUNTROWS, time intelligence  
**Data Modelling:** star-schema semantic model, dimension modelling, date table design, KPI design, drillthrough, conditional formatting  


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

screenshots/07_star_schema.png

## Key Insights

**Overall business health**

**Total Sales: £20.38M** | 62.5K orders | 13.9K customers who placed at least one order  
**AOV: £326**  
**Gross Margin:** 17.2% overall (£3.51M gross profit)  

**Growth is slowing down**

2024: +31.5% year over year
2025: +28.9%
2026: +85.1% — driven almost entirely by a heavy TV-category push in Q2 (tied to a FIFA World Cup promotion). TVs alone accounted for 82% of the entire year's revenue growth — but strip TVs out, and the rest of the business still grew a healthy +17% on its own.
2026 only has data through July (7 months) — June alone accounts for £2.21M of the £6.23M available for the year!

**TVs: the biggest category, but the weakest margin**

TVs = **£4.10M (20.1% of total sales)** — the largest category  
TV margin: **12.8%** — the lowest of all 16 categories (compare: Computer Accessories 29.5%, Smart Tech 26.9%, Fans 23.5%)  
TV growth: £385K (2023) → £463K (2024) → £577K (2025) → **£2.67M (2026, only 7 months!)** — 2026 growth a direct result of the FIFA World Cup  
**Business takeaway:** revenue growth driven mainly by the lowest-margin category is a warning sign, not a win — 2026 is growing in volume but losing profitability compared to 2024/2025  

**Sales channels**

**Website now leads (41.5%)**, ahead of In-Store (33%) and Mobile App (25.5%)  
This reverses the earlier channel order, where In-Store led — a direct consequence of lots of TV orders through our Website/Mobile App

**Promotional campaigns**

**Standard Period = 75.5% of all sales** — day-to-day business, not campaigns, drives the result  
Among promotions: Black Friday keeps growing every year and in 2025 saw the highest total sales value of £672K followed by the summer Sale with £592K  

**Customers**

**79% of customers who ever ordered came back for another order** — a strong loyalty signal across the business  
The **30-44 age group drives the most revenue** (£8.1M, 40% of total) and has a high AOV (£333)  
The **60+ group has the highest average order value** (£349) despite the fewest orders — a small but high-value segment  
Gender split is fairly even: Male £10.62M vs. Female £9.76M (52%/48%)  

**Stores and brands**

Leeds, Birmingham, NDC and Manchester each generate ~£3.6-3.7M — a very even result  
Milton Keynes and London Battersea are slightly behind with ~£2.8M each — solid, but still about 25% behind the other locations  
**Samsung leads all brands** (£2.79M), ahead of Sony (£2.29M) and LG (£1.91M)  



## Next Steps

1. Add row-level security so store managers only see their own store's data.
2. Enhance customer retention analysis with cohort and repeat purchase trends.

---
*Built on a synthetic dataset designed to resemble a real multi-channel electronics retailer, for portfolio purposes only.*
