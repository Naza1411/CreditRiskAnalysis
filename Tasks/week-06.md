# Week 6 — Build a Loan-Month Snapshot

## Assignment to send

Cedar MFB cannot monitor trends from current loan records alone. Build a dataset containing one row per loan per month-end, without using information that was unavailable on that date.

### Learn — maximum 2 hours

Study joins, common table expressions, date functions, window functions, running totals, `ROW_NUMBER`, `LAG`, month-end reporting and point-in-time correctness.

### Build — 6 hours

1. Generate month-end reporting dates covering at least 12 months.
2. Join only loans disbursed by each reporting date.
3. Calculate cumulative scheduled amounts and payments as of that date.
4. Derive outstanding principal, arrears, oldest unpaid due date, DPD, DPD bucket, months on book and loan status.
5. Retain one row per loan per reporting date.
6. Document how closed and written-off loans are treated.

### Submit

- `build_loan_month_snapshot.sql`
- Export of the final snapshot
- Data-lineage diagram
- Validation query results

### Quality checks

- The loan/reporting-date key is unique.
- No future payment affects a historical snapshot.
- Snapshot totals reconcile to independent control queries.
- Months on book cannot be negative.

### Stretch task

Make the query incremental so it can add a new month without rebuilding the full history.

