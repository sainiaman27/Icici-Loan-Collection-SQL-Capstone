# ICICI Bank Loan Repayment & Collection Operations System

SQL Developer capstone built in Google Colab using SQLite, Python (`requests`, `pandas`) and a local internal REST API.

## Problem Statement
Loan operations need an auditable view of scheduled EMIs, received payments, overdue instalments, collection follow-ups and restructuring requests. This project designs the database, consumes an internal API, and builds SQL controls and reports on top of it.

## Dataset
Deterministic synthetic banking data (seed `20260812`, review date `2026-08-01`):
24 branches, 320 customers, 420 loans, 2,940 repayment schedule rows, 3,089 payments, 291 collection actions, 72 restructuring requests.

## What's Covered
| Area | Details |
|---|---|
| Database design | 7-table ER diagram, composite key `(loan_id, installment_no)`, 8 relationships |
| API operations | Filtered GET, POST, PUT, PATCH, GET-DELETE-GET verification |
| SQL analysis (Q1-Q13) | Joins, aggregation, CTEs, subqueries, INTERSECT, CASE, window functions (RANK, DENSE_RANK, LAG, ROW_NUMBER, moving averages) |
| Business logic | Reconciliation (paid/missing/under/overpaid), DPD and delinquency stages, penalty estimate, open exceptions |
| Transactions | COMMIT and ROLLBACK ledger operations |
| Automation | 7-step scheduled workflow, daily top-20 collection-priority report, cron expressions |
| Engineering practices | Git collaboration workflow, safe database-change workflow |

## Results
All 26 validated activities report **Passed** (26/26).

## Tech Stack
Python, SQLite, SQL, pandas, requests, Graphviz, Google Colab

## How to Run
1. Open `AMAN_SAINI_CAPSTONE_PROJECT_SQL.ipynb` in Google Colab (or Jupyter).
2. Runtime -> Run all. Wait for `SETUP COMPLETE`.
3. The final cell prints the progress check.

## Author
Aman Saini
