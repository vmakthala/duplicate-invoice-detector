# Duplicate Invoice Detector (Python)

A small audit analytics project where I used Python (pandas) to find possible duplicate supplier invoices.

## Why this matters
Duplicate payments are a common accounts payable risk. Auditors test for them to check that payments are valid and not paid twice.

## Data
Simulated invoice data (213 invoices, 10 vendors, 2025) created in Python. I planted some duplicates on purpose to test that the checks work.

## What I did
1. Data checks – missing values, data types, total value, negative amounts
2. Test 1 – Exact duplicates
3. Test 2 – Same vendor and amount within 7 days
4. Test 3 – Near-duplicate invoice numbers (e.g. INV-1005 vs INV1005)
5. Combined results into one exception list with £ value at risk

## Results
- 13 exceptions found
- £34,351.53 total value at risk
- Output: `outputs/exceptions.csv` and 2 charts

## Tools
Python, pandas, numpy, matplotlib, Jupyter Notebook

## What I learned
How to turn audit tests into code, and how one invoice can be caught by more than one test, so results need to be de-duplicated before reporting.