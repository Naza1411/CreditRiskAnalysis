## Week 1 - Building the Data Foundation and Understanding the Lending Lifecycle
#### Project Overview

As part of my journey into credit-risk analysis, I am taking on a simulated role as a Junior Credit-Risk Analyst at Cedar MFB, a fictional Nigerian microfinance bank.
## Understanding Risk in Financial Services
Before focusing specifically on credit risk, I first looked at the different types of risk that a financial institution can face.

 Credit risk is the risk that a borrower will fail to meet their financial obligations according to the agreed terms.
 
  For a microfinance bank, examples include:

- A customer failing to repay a loan.
- A customer making only partial repayments.
- A borrower becoming seriously delinquent.
- A loan eventually being written off.

Fraud Risk: Fraud risk relates to intentional deception designed to obtain money, avoid an obligation or manipulate a financial process.
For example, a person could provide false information during a loan application or use another person's identity.

Although fraud and credit risk can sometimes overlap, they are not the same thing. A customer who cannot repay a genuine loan may represent credit risk, while a person who deliberately provides false information to obtain a loan may represent fraud risk.

Operational Risk: Operational risk arises from failures in internal processes, people, systems or external events.
For example: A system incorrectly records a repayment.
An employee enters the wrong loan amount.
A technical failure prevents a payment from being processed.

Liquidity Risk: Liquidity risk is the risk that an institution does not have enough available funds to meet its financial obligations when they become due. For a lender, this is important because the institution needs enough liquidity to meet withdrawals, operating expenses and other obligations.
Market Risk

Market risk: results from changes in market variables such as interest rates, foreign exchange rates or investment prices. Although these risks are important to financial institutions, this project focuses primarily on credit risk and the data needed to monitor it.

Credit risk is the main focus of this project. My first assignment is to understand the business process behind lending and the data generated throughout that process.

Before a credit-risk analyst can calculate delinquency, arrears or portfolio risk, they need to understand where the data comes from, how the different datasets are connected, and what each field represents.

Therefore, Week 1 focused on building the foundation for a credit-risk analysis project.

The central question I explored was:
How does a loan move from application to final repayment or write-off, and what data is produced at each stage?

To answer this, I studied the lending lifecycle, created a data dictionary, built a small synthetic lending dataset in Excel, identified credit-risk questions that could be answered from the data, and performed basic data-quality checks.
## The Cedar MFB Lending Lifecycle
A loan does not simply appear in the system as a loan. It passes through several stages. Understanding the different stages in the lifecycle is important because each stage produces different data.

#### Image of a Lending lifecycle
![alt text](LendingCycle.jpg)