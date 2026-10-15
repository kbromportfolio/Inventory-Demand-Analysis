# Inventory & Demand Analysis

**Project ID:** INV-02  
**Author:** Kbrom Gebremedihin  
**Status:** Project structure and baseline documentation created; data analysis has not started.

This project will analyse the selected retail inventory and demand dataset using Microsoft Excel and Microsoft Power BI. The Markdown proposal is [PERSONAL PROJECT PROPOSAL.md](docs/PERSONAL%20PROJECT%20PROPOSAL.md), converted from the original `docs/PERSONAL PROJECT PROPOSAL.odt`.

## Project management baseline

**PM-01 — Confirm scope and project plan: Complete (15 October 2026).** The baseline proposal and requested folder structure are prepared. Dataset acquisition, provenance, and licence verification are tracked separately under PM-02; `data/raw/sales_data.csv` is present. See the [PM-01 to PM-14 tracker](docs/Project_Management_Plan_INV-02.docx).

## Project structure

```text
Inventory-Demand-Analysis/
├── data/
│   ├── raw/                 # Original source files; never edit in place
│   └── cleaned/             # Validated, separately saved data
├── excel/                   # Inventory_Demand_Analysis.xlsx (to be created)
├── powerbi/                 # Inventory_Demand_Dashboard.pbix (to be created)
├── reports/                 # Reserved for future reports, if needed
├── docs/
│   ├── PERSONAL PROJECT PROPOSAL.md
│   ├── PERSONAL PROJECT PROPOSAL.odt
│   └── Project_Management_Plan_INV-02.docx
└── images/                  # Dashboard preview to be created
```

## Dataset and current status

The proposal identifies `sales_data.csv` from the Kaggle Retail Store Inventory and Demand Forecasting dataset as the intended source ([dataset page](https://www.kaggle.com/dsv/11895299)). A CSV is now present at `data/raw/sales_data.csv`; it has not yet been independently profiled here. Confirm its source and licence/redistribution terms before analysis or publication. Keep the original unchanged and save any cleaned data separately under `data/cleaned/`.

The existing proposal reports an initial profile of 76,000 records, 16 columns, 1 January 2022–30 January 2024, five stores, 20 products, five categories, four regions, no missing values, and no exact duplicate rows. These are **unverified proposal figures**, not results reproduced in this workspace. Verify them against the CSV before reporting them as project findings.

## Tools and workflow

Planned primary tools are Microsoft Excel and Microsoft Power BI. The workflow is to preserve the original CSV, profile and validate it, clean a separate copy, validate KPI calculations, build the Excel analysis, then create the dashboard and evidence-based reports. The [PM-01 to PM-14 tracker](docs/Project_Management_Plan_INV-02.docx) records status, completion date, issues, and Git commit for each task.

## KPI guardrails

Candidate measures include total units sold, total recorded demand, total units ordered, average recorded inventory, zero-inventory record rate, and demand–sales difference. Each definition and aggregation must be checked against the actual data before dashboard use.

- Zero recorded inventory alone does not establish a stockout.
- Demand minus units sold is not confirmed lost sales.
- Units ordered do not necessarily equal units received.
- Inventory turnover will not be reported without validated cost-of-goods-sold and average inventory valuation data.
- Observed associations are not evidence of causation.

## Recommended data documentation

Maintain a data dictionary and cleaning log as analysis proceeds, even though they are not separate project files. Verify the actual CSV's field names, types, units, valid values, nullability, business definitions, and record grain. The proposal anticipates fields for date, store, product, category, region, inventory level, units sold, units ordered, price, discount, weather condition, promotion, competitor pricing, seasonality, epidemic indicator, and demand; confirm these against the file before relying on them.

Keep `data/raw/sales_data.csv` unchanged. For every cleaning action, record the date, field, issue, rationale, row counts before and after, validation performed, and cleaned output path. Check missing values, exact and key duplicates, types, ranges, category consistency, and plausible values; save the cleaned copy separately under `data/cleaned/`.

## Recommended data quality checks

Document the measured results here after profiling the CSV; do not treat proposal-reported figures as verified. Check completeness (including null-like strings), exact-row and candidate-key duplicates, date parsing and coverage, numeric types and plausible ranges, category consistency, and mappings between product, store, and region. Confirm the actual record grain before using a candidate key such as date + store + product. Reconcile important totals and KPI calculations between Excel and Power BI.

Report any issues, their impact, and the action taken. A zero missing-value or exact-duplicate count does not prove the data is logically correct or complete. Confirm field definitions and units from source documentation. Neither zero inventory nor demand greater than units sold independently establishes a stockout or lost sale.

## Recommended business insights

Add findings and recommendations here after profiling the data and validating the relevant KPIs. For each finding, state the business question, measure and comparison, result, and evidence or caveats. Examine demand trends over comparable periods; demand by product and category; recorded demand versus units sold; inventory levels; ordering activity; and observed differences by promotion, discount, price, weather, or season.

Do not fill in results before analysis. Recommendations should follow from validated evidence, not assumptions. A zero-inventory record does not prove a stockout, demand less units sold is not confirmed lost sales, units ordered do not necessarily equal receipts, and observed associations do not establish causation. Report inventory turnover only if the required cost-of-goods-sold and average inventory valuation data are available and validated.

No Excel workbook, Power BI file, or dashboard image has been generated yet; creating empty files with those extensions would imply usable deliverables that do not exist.

## Reports and documentation

- [Project proposal](docs/PERSONAL%20PROJECT%20PROPOSAL.md)
- [Project management plan and tracker](docs/Project_Management_Plan_INV-02.docx)
