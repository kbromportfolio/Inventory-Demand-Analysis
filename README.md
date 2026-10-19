# Inventory & Demand Analysis

**Project ID:** INV-02  
**Author:** Kbrom Gebremedihin  
**Tools:** Microsoft Excel, Microsoft Power BI

## PM-01 — Confirm scope and project plan

Defined and approved the project scope, objectives, methodology, deliverables, tools, schedule, and data-quality safeguards.

**Deliverables**
- [Project proposal](docs/PERSONAL PROJECT PROPOSAL.md)
- [Project management plan](docs/Project_Management_Plan_INV-02.docx)

**Project aim:** Analyse retail inventory and demand data, validate relevant measures, and communicate findings through an interactive dashboard.

## PM-02 — Source and document dataset

Preserved the [raw CSV](data/raw/sales_data.csv) (76,000 records, 16 fields) and recorded its listed source:

- **Dataset:** [Retail Store Inventory and Demand Forecasting](https://www.kaggle.com/datasets/atomicd/retail-store-inventory-and-demand-forecasting)
- **Creator:** Wavelet (`atomicd`)
- **Licence:** Apache 2.0, as listed by Kaggle
- **Source description:** Synthetic inventory and demand forecasting data

The local file has not been verified as an exact copy of a specific Kaggle release. It does not represent confirmed records from a real retailer.

## PM-03 — Profile dataset and inspect fields

Profiled the raw CSV: 76,000 records and 16 fields, dated 1 January 2022–30 January 2024. The data contains 5 stores, 20 products, 5 categories, and 4 regions. No missing values, exact duplicate rows, duplicate date-store-product keys, or negative numeric values were found.

**Data-quality issue:** Every product ID appears with multiple category labels. Product-to-category comparisons should be avoided until this inconsistency is resolved. Zero inventory records do not, by themselves, establish stockouts.

## PM-04 — Clean and prepare data

Preserved the raw CSV and prepared a separate [cleaned file](data/cleaned/sales_data_cleaned.csv). Standardized dates from `dd/MM/yyyy` to ISO `yyyy-MM-dd`; all 76,000 dates parsed successfully. Confirmed 76,000 rows, 16 columns, and unchanged non-date values. No rows were removed.

## PM-05 — Validate data and calculations

Reconciled all 76,000 rows between raw and cleaned files; confirmed no missing values, duplicate rows, or duplicate date-store-product keys. All seven workbook formula checks match independent calculations: units sold (6,750,876), recorded demand (7,928,104), units ordered (6,770,889), average inventory (301.06), zero-inventory record rate (0.53%), and demand less sold (1,177,228). Demand less sold is not confirmed lost sales.

## PM-06 — Create Excel calculations and PivotTables

Added calculated month, demand-gap, and zero-inventory fields, an analysis summary, four PivotTables (monthly, store/region, product, and promotion/seasonality), and a monthly sales-and-demand chart to the [Excel analysis workbook](excel/Inventory_Demand_Analysis.xlsx). Independently checked the PivotTable results against the cleaned CSV. Category comparisons remain excluded because product-to-category mappings are inconsistent.

## PM-07 — Complete exploratory analysis
Initial descriptive findings from the synthetic dataset:
- Average units sold per record were 2.1% lower in 2023 than in 2022; January 2024 is a partial year and is not directly comparable.
- Summer averaged 95.8 units sold per record versus 83.5 in spring.
- Promotion-flagged records averaged 103.1 units sold versus 81.8 without a promotion. This is an association, not evidence that promotions caused higher sales.

These patterns describe the supplied synthetic records only and should not be generalized to real retailers.

## PM-08 — Compare products, stores, regions, and periods

Compared average units sold per record to account for differing group sizes:

- **Products:** Product IDs ranged from 73.1 units (P0020) to 99.9 (P0007) per record, a 36.6% spread. Comparisons use IDs only; category mappings are unreliable.
- **Stores:** S002 averaged 91.2 units per record, the highest; S004 averaged 86.1, the lowest.
- **Regions:** South averaged 91.2 units per record and West 86.1. North contains two stores, so regional totals are not directly comparable.
- **Periods:** The 2023 average was 2.1% below 2022. January 2024 is partial and excluded from full-year comparison.

These are descriptive differences in the synthetic dataset, not evidence of real-world performance.
