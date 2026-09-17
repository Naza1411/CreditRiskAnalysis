# Week 5 — Query a Lending Database with SQL

## Assignment to send

Load the Cedar MFB synthetic tables into a SQL database and answer basic portfolio questions using clear, validated queries.

### Learn — maximum 2 hours

Study `SELECT`, `WHERE`, `CASE`, `GROUP BY`, aggregate functions, null handling, distinct counts and the logical order of SQL execution.

### Build — 6 hours

Write queries that answer:

1. How many applications, approvals and disbursements occurred each month?
2. What are approval, acceptance and disbursement rates?
3. What are total and average principal by product?
4. Which states and channels have the highest exposure?
5. How many active, closed, delinquent and written-off loans exist?
6. Which records contain missing, duplicated or impossible values?

For each answer, state the grain, denominator, date range and exclusions.

### Submit

- SQL table-creation and data-loading script
- `week_05_analysis.sql`
- Query-results workbook or CSV files
- A short memo with three findings and three validation checks

### Quality checks

- Application counts do not inflate after joins.
- Rates use the correct denominators.
- Null decisions and unknown categories are handled explicitly.
- SQL formatting and comments make the work reviewable.

### Stretch task

Create reusable views for the application funnel and loan portfolio.

