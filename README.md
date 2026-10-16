# Inventory & Demand Analysis

**Project ID:** INV-02  
**Author:** Kbrom Gebremedihin  
**Tools:** Microsoft Excel, Microsoft Power BI

Analyse retail demand and inventory data, validate relevant KPIs, and present evidence-based findings in a dashboard.

## Project status

**PM-01 — Confirm scope and project plan:**
 Defined the project aim, objectives, scope, methodology, deliverables, tools, and two-week schedule; established KPI interpretation safeguards and the project folder structure in the baseline proposal.

**PM-02 — Source and document dataset:**
 Placed `sales_data.csv` in `data/raw/` and recorded the proposed Kaggle source. The raw file is preserved unchanged; source provenance and licence terms still need verification before use or publication.

**PM-03 — Initial data profile:**
 Performed initial checks on the raw data and recorded the results in the README. No blank values, parse failures, or duplicates were found in the initial checks. 

## Dataset

Raw data: [`data/raw/sales_data.csv`](data/raw/sales_data.csv)  
Proposed source: [Kaggle — Retail Store Inventory and Demand Forecasting](https://www.kaggle.com/dsv/11895299)

Keep the original CSV unchanged. Confirm provenance, licence, and field definitions before use or publication.

### Initial profile

| Check | Result |
|---|---|
| Size | 76,000 rows, 16 columns |
| Dates | 1 January 2022–30 January 2024 (`dd/MM/yyyy`) |
| Stores / products | 5 / 20 |
| Categories / regions | 5 / 4 |
| Blank values / parse failures | None found in initial checks |
| Exact duplicates / duplicate date-store-product keys | 0 / 0 |

Initial checks are not a substitute for validating business definitions, units, and plausible values.

## Workflow

Preserve and verify the source, profile and clean a separate copy, validate KPI calculations, then build the Excel analysis and Power BI dashboard. Record cleaning decisions and keep the cleaned data in `data/cleaned/`.

## KPI safeguards

Candidate KPIs include units sold, recorded demand, units ordered, and inventory levels. Validate each definition and aggregation before use. Zero inventory does not prove a stockout; demand less units sold is not confirmed lost sales; orders are not necessarily receipts. Do not claim inventory turnover without validated cost-of-goods-sold and inventory valuation data.

## Documentation

- [Project proposal](docs/PERSONAL%20PROJECT%20PROPOSAL.md)
- [Project management plan](docs/Project_Management_Plan_INV-02.docx)

**PM-04 — Clean and prepare data in Excel:**
 Preserved the raw CSV, standardized dates and numeric values, trimmed text, and removed no rows. Created the [cleaned dataset](data/cleaned/sales_data_cleaned.csv) and [Excel workbook](excel/Inventory_Demand_Analysis.xlsx).
