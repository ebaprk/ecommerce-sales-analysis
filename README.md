# E-commerce Sales & Customer Behavior Analysis

A six-part learning project using the UCI Online Retail dataset. The notebooks develop Python/pandas analysis, cleaning decisions, SQL questions, customer metrics, visualizations, and a final case-study exercise.

**Project status:** A guided portfolio workbook with saved outputs and unfinished exercise cells. The presence of a dashboard image or notebook does not mean every exercise or the final written case study is complete.

## Notebook sequence

| Notebook | Focus |
| --- | --- |
| [01 — Explore](notebooks/01_explore_online_retail.ipynb) | Inspect invoice lines, missing values, unusual quantities, and countries. |
| [02 — Clean](notebooks/02_cleaning.ipynb) | Define a positive-sales policy and save a processed CSV. |
| [03 — SQL](notebooks/03_sql_analysis.ipynb) | Create a local SQLite table and write eight business queries. |
| [04 — Customers](notebooks/04_customer_behavior.ipynb) | Repeat customers, invoice values, and distribution comparisons. |
| [05 — Dashboard](notebooks/05_sales_dashboard.ipynb) | Build sales KPIs, a chart dashboard, and recommendations. |
| [06 — Case study](notebooks/06_final_case_study.ipynb) | Audit results, compare complete periods, and prepare a final report. |

## Dataset

Download the Excel workbook from [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail) and save it as:

```text
data/raw/Online Retail.xlsx
```

The workbook and generated data files are excluded from Git. See UCI’s source page for attribution and usage terms. A row represents an invoice line; a complete invoice can contain multiple rows.

## Setup

Python 3.12 is recommended. From a terminal on macOS or Linux:

```sh
git clone https://github.com/ebaprk/ecommerce-sales-analysis.git
cd ecommerce-sales-analysis
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
mkdir -p data/raw data/processed
jupyter notebook
```

On Windows, activate the environment with `.venv\Scripts\Activate.ps1` in PowerShell. Alternatively, open the repository in VS Code with the Python and Jupyter extensions and choose `.venv` as the notebook kernel.

Work through the notebooks in order. Read each worked example, write your own code in the exercise cells, and complete the written interpretations. Later notebooks require `data/processed/valid_sales.csv` from the cleaning notebook. SQLite runs locally through Python’s standard library; no database server is required.

## Outputs and metric definitions

- [SQL working file](sql/analysis_queries.sql).
- [Saved dashboard image](dashboard/week5_sales_dashboard.png).
- [Report charts](reports/).
- `reports/final_case_study.md` is a target deliverable for the final notebook; it is not currently included.

Positive-sales revenue uses the retained line quantities and prices after the documented exclusions. It is distinct from net accounting revenue because returns and cancellations are set aside. Count distinct `InvoiceNo` values for orders. Customer-level measures exclude missing customer IDs; keep that denominator separate from overall sales totals. Compare complete months fairly rather than treating partial-month totals as equivalent exposure.

## Folder guide

```text
notebooks/       Guided analysis and exercises
sql/             SQL working queries
dashboard/       Saved dashboard image
reports/         Saved charts and future written findings
requirements.txt Python dependencies
```

Create `data/raw/` and `data/processed/` locally. Keep the original workbook unchanged so the cleaning decisions remain reproducible.
