## Week 2-Loan Repayment & Amortisation Analysis
## Overview
In Week 2, I developed an Excel-based loan repayment and amortisation model for Cedar MFB. The objective was to understand how loan pricing and repayment methods affect instalments, total repayment, outstanding balances and borrower affordability.

I worked with a portfolio of **10 loan records** and used the available loan information to build and validate repayment schedules under two different interest methods: **flat-rate** and **reducing-balance**.

## What I Built

### 1. Loan Data & Input Validation

I created a validation layer to check the quality and consistency of the loan data before using it in the repayment calculations.

The validation checks included:

* Missing Loan IDs and Customer IDs
* Invalid or non-positive principal amounts
* Invalid annual interest rates
* Negative processing fees
* Missing or invalid disbursement dates
* Invalid loan terms
* Invalid monthly interest rates
* Differences between the stated instalment and the calculated flat-rate repayment amount

The calculated total repayment was reconciled against the provided instalment using:

**Flat-rate Total = Principal + (Principal × Monthly Interest Rate × Term) + Fee**

All **20 loans passed the validation checks**, with no missing or inconsistent entries identified.
## 2. Flat-Rate Amortisation Schedule

I built a separate flat-rate repayment schedule for each loan.

Under the flat-rate method, monthly interest is calculated using the **original principal throughout the loan term**, rather than the remaining balance.

Each schedule contains:

* Loan ID
* Month number
* Due date
* Opening balance
* Principal repayment
* Interest
* Processing fee
* Total instalment
* Closing balance

The processing fee is charged once in the first repayment period.

For example, for a ₦50,000 loan at a 4% monthly rate over three months, the interest is calculated on the original ₦50,000 for each month.

---

## 3. Reducing-Balance Amortisation Schedule

I also created a reducing-balance repayment schedule using the **PMT/EMI approach**.

Unlike the flat-rate method, interest is calculated on the outstanding loan balance. As the principal decreases, the interest component of the repayment also decreases.

The schedule contains the same key fields:

* Due date
* Opening balance
* Principal
* Interest
* Fee
* Total instalment
* Closing balance

This allowed me to compare how the same loan behaves under different interest calculation methods.

---

## 4. Scenario Comparison

To understand the effect of loan size and tenor, I compared three scenarios using a **48% annual rate / 4% monthly rate**:

| Scenario | Principal |      Term | Flat Total Repayment | Reducing-Balance Total |  Difference |
| -------- | --------: | --------: | -------------------: | ---------------------: | ----------: |
| 1        |   ₦50,000 |  3 months |              ₦57,000 |             ₦55,052.28 |   ₦1,947.72 |
| 2        |  ₦150,000 |  6 months |             ₦191,000 |            ₦176,685.71 |  ₦14,314.29 |
| 3        |  ₦500,000 | 12 months |             ₦752,500 |            ₦651,813.04 | ₦100,686.96 |

For the ₦500,000/12-month scenario, a **₦12,500 processing fee** was used as an assumption because there was no matching ₦500,000 loan in the portfolio. The assumption was made using a 2.5% fee-to-principal ratio observed among larger loans in the dataset and was left editable in the workbook.

---

## 5. Affordability Analysis

I calculated both the average monthly instalment under the flat-rate method and the EMI under the reducing-balance method.

For the three scenarios:

* **₦50,000 for 3 months:** flat monthly repayment = ₦19,000; reducing-balance EMI ≈ ₦18,017.
* **₦150,000 for 6 months:** flat monthly repayment ≈ ₦31,833; reducing-balance EMI ≈ ₦28,614.
* **₦500,000 for 12 months:** flat monthly repayment ≈ ₦62,708; reducing-balance EMI ≈ ₦53,276.

The analysis showed that the difference between the two methods becomes more significant as **loan size and repayment period increase**.

The effective cost of the flat-rate method in the scenarios was approximately **14.0%, 27.3% and 50.5% of principal**, compared with approximately **10.1%, 17.8% and 30.4%** under reducing balance.

---

## Key Learning

The main lesson from this exercise was that the **headline interest rate alone does not provide a complete picture of borrowing cost**.

A 4% monthly flat-rate loan and a 4% monthly reducing-balance loan use the same stated rate but produce different total repayment amounts because interest is calculated on different balances.

With a flat rate, interest continues to be calculated on the original principal even after part of the principal has been repaid. With reducing balance, interest is recalculated based on the outstanding principal.

This means that when comparing loan products, I need to consider:

* Interest calculation method
* Total interest
* Processing fees
* Total repayment
* Monthly repayment obligation
* Loan tenor
* Effective cost relative to the amount borrowed


## Week 2 Outcome

By the end of Week 2, I had transformed the raw loan data into a structured repayment model that could calculate, validate and compare different loan repayment methods.

The workbook provides an auditable way to examine how **principal, interest, fees, loan tenor and repayment methodology** affect the total cost and monthly repayment burden of a loan.

#Dataset
[text](<Input Data.xlsx>)