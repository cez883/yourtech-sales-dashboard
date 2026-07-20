# YourTech.com — Sales Performance Dashboard (Power BI)

## Executive Summary

Built a 6-page Power BI dashboard for YourTech.com, a fictional multi-channel electronics retailer, to give sales, marketing, and product stakeholders a single place to answer their recurring questions — instead of relying on scattered spreadsheet exports.

<img width="1955" height="1096" alt="image" src="https://github.com/user-attachments/assets/c63be6af-e117-4a25-966d-ca0634114d0b" />

## Business Problem

Stakeholders across the business kept asking the same recurring questions, each pulling data a different way:

- **Sales:** How is revenue trending, and which channels and categories drive it?
- **Marketing:** Which campaigns pay off, and do bigger discounts actually help?
- **Customer:** Who are our customers, and how does spending differ by age and gender?
- **Product/merchandising:** Which products and brands are most profitable?
- **Support/account management:** What is a specific customer's full order history?

The goal was one report that answers all of these consistently, with the ability to drill from a summary view down to an individual customer's order history.

## Methodology

1. For the purpose of this project I have created a dataset containing three .csv files: Customers, Sale_Event as well as YourTech_Orders containing over 100k rows of sale transactions data.
2. I have imported the data into Power BI and used Power Query to clean, transform and prepare data for further analysis
3. I have crerated a star schema semantic model (`fSales` fact table with `dCustomers`, `dProducts`, `dDate`, `dStores`, `dStaff`, `dSale Event` dimensions) and created relationships between these tables
4. Built DAX measures for sales, profit, campaign performance, and customer metrics, including time intelligence (YoY, YTD).
5. Designed 6 report pages, each mapped to a specific set of business questions.
6. Added a drillthrough page so any customer can be opened directly from a summary table to see their full order history.
7. Applied conditional formatting (colour-scale heatmap) and consistent slicer behaviour across pages for a smoother user experience.

## Skills

**Power Query:** ETL, data cleaning, locale-aware date parsing
**DAX:** CALCULATE, RANKX, TOPN, SELECTEDVALUE, time intelligence
**Power BI:** star-schema data modelling, drillthrough, conditional formatting, slicer design, report UX

## Report Pages

| Page | Business questions it answers |
|---|---|
| **Sales Performance** | Overall sales trend, channel mix, category mix, top products |
| **Campaign Performance** | Which promotions drive sales/profit, and whether discounts pay off |
| **Customer Insights** | Who buys, spending patterns by age and gender, top customers |
| **Product & Brand Insights** | Top products, brands, and category profitability |
| **Customer Order Details** *(drillthrough)* | Full order history and lifetime value for a single customer |
| **Business Questions** | Index page mapping each question to the right report page |

## Key Insights

<img width="1952" height="1094" alt="image" src="https://github.com/user-attachments/assets/5763a3bb-9ee4-4dd2-9f03-c1cd3fd8234e" />

- **In-Store is the leading sales channel**, followed by Website and Mobile App.
- **Mobile Phones is the top-performing product category** by revenue, ahead of Fridge Freezers and Laptops.
- **Standard (non-campaign) periods drive the majority of annual revenue** — promotional campaigns like Black Friday and Summer Sale are meaningful but secondary contributors.
- **Spending peaks in the 30-44 and 45-59 age groups**, both in average order value and total revenue.

## Next Steps

1. Add row-level security so store managers only see their own store's data.
2. Extend customer analysis with retention/tenure metrics based on first purchase date.
3. Publish to Power BI Service with scheduled data refresh.

---
*Built on a synthetic dataset designed to resemble a real multi-channel electronics retailer, for portfolio purposes only.*
