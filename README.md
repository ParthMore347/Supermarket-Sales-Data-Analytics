# Supermarket Sales Analysis - Executive Decision Dashboard
**Author:** Parth More  
**Program:** IBM SkillsBuild Academic Internship – Data Analytics with AI  
**Partner:** AICTE & BharatCares  

## 1. Overview

This project applies an end-to-end Data Analytics workflow to retail supermarket transaction data. It combines data loading, cleaning, KPI computation, visualization, risk identification, and executive reporting in Python. The analysis follows the 5-Level Decision Dashboard framework:

1. **Executive KPIs:** establish the commercial baseline.
2. **Trends:** show when revenue is generated.
3. **Drivers:** explain product and branch performance.
4. **Risk Analysis:** identify rating and performance risks.
5. **Actionable Recommendations:** convert evidence into decisions using Fact → Insight → Opportunity → Action.

The project produces both an analytical Jupyter Notebook and a reusable Python report generator that creates PNG charts and a formatted Word report.

## 2. Dataset Information

- **Source link:** https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales
- **Details:** 1,000 transactions across 3 city branches (Yangon, Naypyitaw, Mandalay).
- **Primary measures:** invoice ID, branch, city, product line, unit price, quantity, total, date, time, payment, and customer rating.
- **Runtime source:** the report script loads the published CSV from GitHub:
  https://raw.githubusercontent.com/aungpyaeap/supermarket-sales/master/supermarket_sales%20-%20Sheet1.csv

## 3. Directory Structure

```text
ParthMore_SupermarketSales.ipynb
generate_report.py
ParthMore_ProjectReport.docx
README.md
requirements.txt
report_images/
├── kpi_summary.png
└── revenue_by_product.png
```

`ParthMore_ProjectReport.docx` and the PNG files are generated when `generate_report.py` runs.

## 4. Setup & Execution Instructions

### Windows PowerShell

From the workspace root:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Launch the notebook:

```powershell
jupyter notebook
```

Run the automated report generator:

```powershell
python generate_report.py
```

### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter notebook
python generate_report.py
```

The script creates `report_images/`, saves `kpi_summary.png` and `revenue_by_product.png`, and writes `ParthMore_ProjectReport.docx` to the workspace root.

## 5. Executive Recommendations Summary

- **Fact:** The leading product line contributes the most revenue.  
  **Insight:** Revenue is concentrated in a category with proven demand.  
  **Opportunity:** Increase basket size with complementary products.  
  **Action:** Test cross-sell bundles and measure Average Order Value over four weeks.

- **Fact:** The lowest-revenue product line trails the category leaders.  
  **Insight:** Visibility, assortment, or pricing may be limiting demand.  
  **Opportunity:** Recover revenue through a focused intervention instead of broad discounting.  
  **Action:** Run a targeted end-cap or price test with a control period.

- **Fact:** Categories with ratings below the overall average are potential experience risks.  
  **Insight:** Unresolved category-level issues can reduce repeat purchase and increase churn.  
  **Opportunity:** Use customer feedback to identify the root cause.  
  **Action:** Create category-specific improvement plans and monitor rating recovery.

