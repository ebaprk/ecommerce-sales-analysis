# E-commerce Sales Performance & Customer Behavior Analysis

A beginner-friendly portfolio project using the UCI Online Retail dataset. The goal is to learn how to inspect transaction data with Python, then build toward business questions about sales trends, products, countries, and repeat purchasing.

## Project status

Week 1 exploration is complete. The notebook records the initial data checks and written observations. The dataset is not included in this repository; download it from the [UCI Online Retail dataset page](https://archive.ics.uci.edu/dataset/352/online+retail) and save the Excel file as:

`data/raw/Online Retail.xlsx`

Keep the original workbook in `data/raw/`. The `.gitignore` file prevents raw and processed data files from being uploaded to GitHub.

## Folder guide

- `data/raw/` — original downloaded data (kept out of Git)
- `data/processed/` — cleaned or derived data (kept out of Git)
- `notebooks/` — learning and analysis notebooks
- `src/` — reusable Python code as the project grows
- `sql/` — SQL queries for later analysis
- `dashboard/` — dashboard files and screenshots
- `reports/` — written findings and recommendations

## Setup on macOS

Open Terminal and move into this project folder:

```bash
cd "/Users/abepark/Documents/Codex/2026-10-28/referenced-chatgpt-conversation-this-is-an/ecommerce-sales-analysis"
```

A virtual environment is the project’s private Python setup. The `.venv/` folder holds the interpreter and libraries for this project, so other projects can use different versions without conflicts.

Create and activate the local virtual environment:

```bash
python3.12 -m venv .venv
source .venv/bin/activate
```

Install the project libraries:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --prefix .venv --name ecommerce-sales-analysis --display-name "Python (ecommerce-sales-analysis)"
```

In VS Code, open this folder. The local workspace settings point Python to `.venv/bin/python`. To use notebooks in VS Code, install the Microsoft Python and Jupyter extensions if VS Code prompts you for them, then select the `.venv` kernel when prompted. The `.vscode/` folder is local-only and is excluded from Git.

To leave the environment when you are done, run `deactivate` in Terminal.

## First notebook

Start with `notebooks/01_explore_online_retail.ipynb`. The first cells load the workbook; after that, you write your own code to explore the columns, missing values, unusual quantities, invoice counts, and country filters. Short hints and spaces for written observations guide you through Week 1.

## Planned analysis questions

1. How much revenue is represented by the recorded transactions?
2. How do sales change over time?
3. Which products and countries contribute most to sales?
4. How often do customers return to purchase again?
5. What practical recommendations follow from the analysis?

## Publishing to GitHub

A useful first upload includes this README, `.gitignore`, `requirements.txt`, notebooks, SQL queries, reusable source code, dashboard materials, and a short report. Do not upload the downloaded workbook or private environment files. Cite UCI as the dataset source in your final report.
