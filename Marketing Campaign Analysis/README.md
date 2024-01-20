# Marketing Campaign Analysis

## Table of content
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Cleaning/Prepration](#data-cleaningprepration)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendations)

## Project Overview
XYZ Paints Inc. is a paint company which was recently launched in 2019. Since then, they have established their name in top tier 1 and 2 cities (slowly expanding to tier 3 cities as well). 

They have orders coming from household, industrial and government sectors. In recent years, they are seeing quite a steady growth and would like to continue that in future. 

They have hired you as a Data Scientist in their data consulting team which offers services across various departments such as sales, marketing, logistics, etc. 


They have given you a sample of data from their databases. You have to work on some of the pain points of the marketing team like consumer growth, lead conversions, etc. as well as help them work on new set of campaigns or doing market basket analysis.

## Data Source
Name of the tables:
- Customer
- Item
- CustomerTransactionData
- CouponMapping
- CityData
- Campaign
  
Dataset schema
![schema](https://github.com/atul139/SQL_Projects/assets/121300861/9b8b1fa0-e1b8-417f-bec2-a26f04368145)

## Data Analysis
I have worked with the following concepts:
- Data Filtering with SQL Operators 
- Aggregating and Sorting Functions 
- String, Math, and DateTime Functions
- JOINS and Subqueries
- Windows Function
- Case Statement, Procedures, Functions and Views

## Tools
Metabase

## Data Cleaning/Prepration
- Data loading and inspectiom
- Handling missing values
- Data cleaning and formatting

## Exploratory Data Analysis
EDA involve exploring the sales data to answer key questions, such as:
- Consumer growth
- Lead conversions
- Setting up new campaigns
- Market basket analysis

## Results/Findings
- Max sales is for Oil paint and Min sales is for Synthetic paint
- Number of transactions with coupons is 186 while without coupons is 114.
- Based on Quantity of paint that's sold,Company made a steady growth in the past 2 years and saw a declining pattern in the current year.
- Household order type has done exceptionally well in acquiring new and retaining existing customers compared to rest of the 2 order type

## Recommendations
Based on the Analysis, below are the recommendations provided:
- Item 16 and Item 13, Item 9 and Item 45, Item 14 and Item 35 are being bought frequently together amongst different sectors. Especially in households, we have seen quite a good demand for these products. We can try to promote all the 3 in the household sector and the first combination in all the sectors.
