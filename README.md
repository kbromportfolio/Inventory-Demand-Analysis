# Inventory & Demand Analysis

**Project ID:** INV-02  
**Author:** Kbrom Gebremedihin  
**Tools:** Microsoft Excel, Microsoft Power BI

Analyse retail demand and inventory data, validate relevant KPIs, and present evidence-based findings in a dashboard.

## Project status

1. **PM-01 — Confirm scope and project plan — Complete.** Defined the project aim, objectives, scope, methodology, deliverables, tools, schedule, and KPI safeguards.
2. **PM-02 — Source and document dataset — In progress.** Preserved the source CSV and recorded the proposed Kaggle dataset. Verify licence terms before use or publication.
3. **PM-03 — Profile dataset and inspect fields — Complete.** Profiled 76,000 records and 16 fields; results are summarized below.
4. **PM-04 — Clean and prepare data in Excel — Complete (16 October 2026).** Standardized dates and numeric values, trimmed text, and removed no rows. Created the cleaned CSV and Excel workbook.
5. **PM-05 — Validate data and calculations — Complete (16 October 2026).** Reconciled the raw and cleaned files row by row and checked key totals and KPIs against independent calculations; all seven workbook checks passed. Identified inconsistent product-to-category mappings for follow-up.
6. **PM-06 — Create Excel calculations and PivotTables — Planned.** Build analysis formulas, PivotTables, and charts from validated data.
7. **PM-07 — Complete exploratory analysis — Planned.**
8. **PM-08 — Compare products, stores, regions, and periods — Planned.**
9. **PM-09 — Define and validate KPIs — Planned.**
10. **PM-10 — Build Power BI dashboard — Planned.**
11. **PM-11 — Interpret results and prepare recommendations — Planned.**
12. **PM-12 — Complete project documentation — In progress.**
13. **PM-13 — Organise and publish GitHub repository — Planned.**
14. **PM-14 — Review, test, and finalise project — Planned.**

## Dataset

Raw data: [`data/raw/sales_data.csv`](data/raw/sales_data.csv)  
Cleaned data: [`data/cleaned/sales_data_cleaned.csv`](data/cleaned/sales_data_cleaned.csv)  
Excel workbook: [`excel/Inventory_Demand_Analysis.xlsx`](excel/Inventory_Demand_Analysis.xlsx)  
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

### PM-05 validation results

The raw and cleaned files match row by row across all 76,000 records and 16 fields. No blank cells, parsing errors, duplicate rows, or duplicate date-store-product keys were found. Excel formula results matched independent calculations for row count, units sold (6,750,876), recorded demand (7,928,104), units ordered (6,770,889), average inventory (301.06), zero-inventory record rate (0.53%), and demand less units sold (1,177,228).

**Issue to investigate:** All 20 Product IDs appear with multiple Category values. Do not rely on product/category comparisons until this source-data inconsistency is understood. Demand less units sold is not confirmed lost sales.

## Workflow

Preserve and verify the source, profile and clean a separate copy, validate KPI calculations, then build the Excel analysis and Power BI dashboard. Record cleaning decisions and keep the cleaned data in `data/cleaned/`.

## KPI safeguards

Candidate KPIs include units sold, recorded demand, units ordered, and inventory levels. Validate each definition and aggregation before use. Zero inventory does not prove a stockout; demand less units sold is not confirmed lost sales; orders are not necessarily receipts. Do not claim inventory turnover without validated cost-of-goods-sold and inventory valuation data.

## Documentation

- [Project proposal](docs/PERSONAL%20PROJECT%20PROPOSAL.md)
- [Project management plan](docs/Project_Management_Plan_INV-02.docx)

