# Week 3 — Calculate Arrears and Days Past Due

## Assignment to send

Cedar MFB has scheduled instalments and actual payments. Create a repayment tracker that allocates payments, identifies unpaid obligations and calculates days past due as of a selected reporting date.

### Learn — maximum 2 hours

Study arrears, due versus paid amounts, partial payments, oldest unpaid due date, days past due, delinquency buckets, cure and write-off. Note that lenders may use different contractual allocation rules, which must be documented.

### Build — 6 hours

1. Expand the synthetic data to at least 20 loans and 60 instalments.
2. Include on-time, late, partial, missed, prepaid and cured examples.
3. Choose and document a payment-allocation rule.
4. Calculate cumulative due, cumulative paid, arrears, oldest unpaid due date and DPD at a user-selected reporting date.
5. Assign Current, 1–7, 8–30, 31–60, 61–90 and 90+ buckets.
6. Produce an exception list for impossible dates, duplicate IDs, overpayments and negative balances.

### Submit

- `loan_repayment_tracker.xlsx`
- A tab explaining the formulas and allocation rule
- Exception report
- Three portfolio observations

### Quality checks

- DPD is never negative.
- Total payments reconcile to the payment table.
- The oldest unpaid due date changes correctly after a cure.
- Reporting dates do not use future payments.

### Stretch task

Compare loan-level DPD under first-in-first-out and proportional payment allocation.

