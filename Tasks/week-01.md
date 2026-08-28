# Week 1 — Understand the Lending Lifecycle and Its Data

## Assignment to send

You are joining Cedar MFB as a junior credit-risk analyst. Your first task is to explain how a loan moves from application to final repayment or write-off, and identify the data produced at each step.

### Learn — maximum 2 hours

Study the difference between credit, fraud, operational, liquidity and market risk. Learn the stages of application, underwriting, approval, disbursement, repayment, collections, recovery and write-off. Learn what “data grain” means.

### Build — 6 hours

1. Draw a one-page lending lifecycle.
2. Create a data dictionary for the six tables in the shared case study.
3. For every field, state its meaning, type, grain, example value and whether it contains sensitive information.
4. Create 10 sample customers, 15 applications and 8 loans in Excel.
5. Write five questions a credit-risk analyst could answer from the data and identify the tables required.

### Submit

- Lending lifecycle diagram
- `cedar_data_dictionary.xlsx`
- Small synthetic dataset
- A one-page note explaining data grain and the difference between credit risk and fraud risk
- Updated repository README

### Quality checks

- IDs are unique at their intended grain.
- Applications can exist without loans, but every loan links to an application and customer.
- Dates follow a logical order.
- All data is fictional.

### Stretch task

Add data-owner, refresh-frequency and validation-rule columns to the dictionary.

