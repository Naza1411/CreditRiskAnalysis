# Week 5 - Querying a Lending Database with SQL

## Overview

In Week 5, I moved the Cedar MFB credit-risk project from Excel-based analysis into a SQL database. The goal was to load the synthetic lending data into relational tables and use SQL to answer basic portfolio and data-quality questions.

This exercise focused on writing clear, auditable queries that produce reliable portfolio metrics while avoiding common issues such as inflated counts, incorrect denominators, and poorly handled missing values.

## What I Learned

I practised using:

* `SELECT` and `WHERE` for retrieving and filtering records
* `CASE` for classification and conditional logic
* `GROUP BY` and aggregate functions for portfolio summaries
* `COUNT`, `SUM`, and `AVG` for calculating key metrics
* `COUNT(DISTINCT ...)` to prevent duplicate counting
* `NULL` handling and explicit treatment of unknown categories
* SQL execution order and how joins can affect results

## What I Built

I created SQL queries to analyse the Cedar MFB lending portfolio, including:

1. Monthly applications, approvals, and disbursements
2. Approval, acceptance, and disbursement rates
3. Total and average principal by loan product
4. Exposure by state and acquisition channel
5. Loan status across active, closed, delinquent, and written-off accounts
6. Data-quality checks for missing, duplicated, and impossible values

For each analysis, I documented the relevant data grain, denominator, date range, and exclusions to make the results easier to validate and reproduce.

## Data Validation

A key part of the exercise was ensuring that the SQL results were reliable. I checked that:

* Application counts were not inflated by joins.
* Rates used the appropriate denominators.
* Null decisions and unknown categories were handled explicitly.
* Duplicate and impossible records could be identified.
* Queries were formatted and commented for review.

## Deliverables

The Week 5 project contains:

* SQL table-creation and data-loading scripts
* `week_05_analysis.sql`
* Query-result files in workbook/CSV format
* A short analytical memo containing three findings and three validation checks

## Stretch Task

I also explored creating reusable SQL views for the **application funnel** and **loan portfolio**, making commonly used analyses easier to query and reproduce.

## Key Takeaway

Week 5 strengthened my ability to move from spreadsheet-based credit analysis to database-driven analysis. I learned that reliable SQL analysis is not only about writing queries that return results, but also about understanding data grain, choosing correct denominators, controlling for duplication, and validating the underlying data.
