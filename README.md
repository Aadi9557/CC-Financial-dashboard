# Credit Card Customer & Transaction Analytics

A portfolio analytics project exploring customer profiles, credit-card activity, spending behaviour, card usage, revenue-related measures, and delinquency indicators using a sample dataset.

> **Data note:** The files in this repository are sample/training data, as confirmed by the project owner. They are not presented as live customer or bank records.

## Project overview

This project brings together customer attributes and credit-card transaction measures to support business questions such as:

- Which card categories and customer segments contribute most to transaction activity?
- How do transaction amount and transaction volume vary across spending categories?
- How does credit utilisation differ across customer groups?
- What patterns appear in activation, annual fees, and customer acquisition cost?
- How are delinquency indicators distributed across the sample?

The repository includes PDF report outputs and CSV source tables. The exact dashboard authoring file and refresh workflow are not currently included in the repository.

## Repository contents

| File | Description |
|---|---|
| `Credit Card Customers Report.pdf` | Customer-focused report output |
| `Credit Card Transection Report.pdf` | Transaction-focused report output (original filename retained) |
| `customer.csv` | Customer profile and demographic attributes |
| `cust_add.csv` | Additional customer attributes |
| `credit_card.csv` | Card, usage, transaction and delinquency measures |
| `cc_add.csv` | Additional card and transaction attributes |

## Data model at a glance

### Customer tables

The customer datasets include fields such as:

- Customer age and gender
- Dependants, education and marital status
- State code and ZIP code
- Car and home ownership indicators
- Personal loan indicator
- Customer job and income
- Customer satisfaction score

### Credit-card and transaction tables

The card datasets include fields such as:

- Card category and annual fees
- Activation within 30 days
- Customer acquisition cost
- Credit limit and revolving balance
- Transaction amount and transaction volume/count
- Average utilisation ratio
- Transaction channel and expense type
- Interest earned and delinquency indicator
- Week, quarter and year attributes

Column names vary slightly between the supplied files. Review the source headers and data types before combining tables.

## Suggested analysis framework

| Analysis area | Example measures |
|---|---|
| Portfolio overview | Customer count, total transaction amount, total transaction count |
| Card performance | Customers and activity by card category |
| Customer segmentation | Age bands, income bands, occupation, geography |
| Spending behaviour | Transaction amount and volume by expense type |
| Credit utilisation | Average utilisation, revolving balance and credit limit |
| Acquisition and activation | Acquisition cost and 30-day activation rate |
| Risk indicators | Delinquency rate and segment-level distribution |
| Customer experience | Average satisfaction score by segment |

These are suggested analytical questions and measures, not claims about findings already established by the report.

## Recommended dashboard pages

1. **Executive overview** — portfolio KPIs and period trends.
2. **Customer profile** — age, income, occupation, geography and satisfaction.
3. **Card and transaction performance** — card category, spend, transaction count and expense type.
4. **Credit utilisation** — credit limit, revolving balance and utilisation.
5. **Risk and activation** — delinquency indicators and activation performance.

## Data preparation considerations

Before analysis or refresh:

- Confirm the relationship keys and row granularity of each table.
- Check whether `Client_Num` is unique in each customer-level table.
- Check for duplicate records and missing values.
- Standardise date formats, numeric types, categorical labels and whitespace.
- Validate whether transaction fields represent counts, amounts or volumes.
- Avoid summing customer-level attributes after joining them to transaction-level rows; this can inflate totals.
- Document any filters, exclusions, assumptions and calculated measures.

## Tools and deliverables

**Repository assets:** CSV datasets and PDF report outputs.

**Suggested analysis environment:** Power BI for data modelling, DAX measures and interactive reporting; Excel or SQL for data checks and preparation.

The PBIX source file, screenshots of interactive report pages, and a reproducible data-refresh guide are not currently listed in this repository. Add them when available so reviewers can inspect and reproduce the analysis.

## Reproducibility checklist

- [ ] Document source and licence for the sample dataset.
- [ ] Define table relationships and granularity.
- [ ] Validate KPI calculations against the source data.
- [ ] Add the editable dashboard file, if available.
- [ ] Add screenshots of the report pages.
- [ ] Record refresh and transformation steps.
- [ ] Verify that no credentials or non-sample personal data are committed.

## Author

**Aadi9557**

---

*Built as a learning and portfolio project to demonstrate data preparation, business analysis, KPI design and dashboard storytelling.*
