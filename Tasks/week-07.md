# Week 7 — Create a SQL Credit-Metrics Pack

## Assignment to send

Use the loan-month snapshot to calculate Cedar MFB's standard monthly risk metrics and make every definition auditable.

### Learn — maximum 2 hours

Study exposure, unit and value delinquency, PAR 30, 1+/30+/90+ DPD, collection rate, cure rate, default rate, recovery rate and write-off rate. Distinguish stock metrics from flow metrics.

### Build — 6 hours

1. Create a metric dictionary with formula, grain, numerator, denominator, timing and exclusions.
2. Write monthly queries for active accounts, disbursement, outstanding balance, average loan size, collection rate, 1+, 30+, 90+, PAR 30, defaults and write-offs.
3. Segment the metrics by product, risk band and channel.
4. Create automated checks for duplicate keys, invalid DPD, missing products and total-to-segment reconciliation.
5. Explain why two reasonable definitions of at least one metric could produce different results.

### Submit

- `credit_metrics.sql`
- Metric dictionary
- Monthly metric output
- 300-word risk commentary

### Quality checks

- Metric denominators are explicitly stated.
- Segment totals reconcile to overall totals.
- Rates use eligible populations, not every historical record.
- Default and write-off are not treated as identical without explanation.

### Stretch task

Add prior-month values and month-on-month changes using window functions.

