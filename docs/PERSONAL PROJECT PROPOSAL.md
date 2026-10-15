# Personal Project Proposal

## Inventory & Demand Analysis

| Project detail | Value |
|---|---|
| Project ID | INV-02 |
| Project author | Kbrom Gebremedihin |
| Project type | Personal Data Analytics and Business Intelligence Project |
| Academic standard | Undergraduate / BSc-Level Applied Project |
| Industry | Inventory Management and Supply Chain Analytics |
| Primary tools | Microsoft Excel and Microsoft Power BI |
| Supporting tools | Git and GitHub |
| Project duration | 2 weeks |
| GitHub repository | Inventory-Demand-Analysis |
| Proposal date | October 15, 2026 |

## Table of contents

1. [Introduction](#1-introduction)
2. [Background and Business Problem](#2-background-and-business-problem)
3. [Project Aim](#3-project-aim)
4. [Project Objectives](#4-project-objectives)
5. [Dataset Description](#5-dataset-description)
6. [Project Scope](#6-project-scope)
7. [Methodology](#7-methodology)
8. [Data Quality and Validation](#8-data-quality-and-validation)
9. [Key Performance Indicators](#9-key-performance-indicators)
10. [Analysis and Dashboard Requirements](#10-analysis-and-dashboard-requirements)
11. [Project Deliverables](#11-project-deliverables)
12. [Project Management Plan](#12-project-management-plan-pm-01-to-pm-14)
13. [Expected Outcomes](#13-expected-outcomes)
14. [Limitations and Assumptions](#14-limitations-and-assumptions)
15. [Future Development](#15-future-development)
16. [Conclusion](#16-conclusion)

## 1. Introduction

Inventory management and demand analysis are important business functions that help organisations understand product demand, monitor inventory levels, evaluate sales activity, and make informed operational decisions.

This project will analyse a retail inventory and demand dataset using Microsoft Excel and Microsoft Power BI. It will apply data cleaning, data validation, exploratory analysis, KPI calculations, visualisation, and basic demand forecasting where appropriate.

The project is designed to demonstrate practical data analytics and business intelligence skills through a structured, reproducible workflow. It will also provide a portfolio example relevant to Data Analyst, Inventory Analyst, Supply Chain Analyst, and Warehouse Data Analyst roles.

## 2. Background and Business Problem

Retail businesses need to understand how demand changes across products, stores, categories, regions, and time periods. Poor visibility of these patterns can make inventory planning more difficult and may contribute to excess stock, insufficient stock, or inefficient ordering decisions.

The dataset contains daily records associated with stores and products, including inventory levels, units sold, units ordered, demand, prices, discounts, promotions, and contextual factors.

The project will investigate what these records reveal about demand patterns and inventory indicators. It will transform the raw data into structured analysis and an interactive Power BI dashboard that communicates findings clearly.

The analysis will distinguish between directly measured results and indicators that require further validation. It will not assume that every inventory or stockout measure can be calculated from the available data.

## 3. Project Aim

To analyse retail inventory and demand data using Microsoft Excel and Microsoft Power BI to identify demand patterns, examine inventory indicators, evaluate relevant business factors, and communicate evidence-based insights through an interactive dashboard.

## 4. Project Objectives

The project will aim to:

- Inspect and understand the structure and quality of the dataset.
- Validate dates, numerical fields, categorical values, and record uniqueness.
- Clean and prepare the dataset using Microsoft Excel.
- Analyse demand and units sold across products, categories, stores, regions, and time.
- Examine recorded inventory levels and ordering activity.
- Investigate relationships between demand and available contextual variables, including promotions, discounts, prices, weather, and seasonality.
- Develop clearly defined KPIs supported by the available fields.
- Build an interactive Power BI dashboard.
- Explore basic demand forecasting if the time series is suitable.
- Document findings, limitations, recommendations, and the complete project workflow.
- Publish the project documentation and appropriate outputs on GitHub.

## 5. Dataset Description

**Dataset filename:** `sales_data.csv`  
**Dataset source:** Kaggle — Retail Store Inventory and Demand Forecasting dataset  
**Source link:** <https://www.kaggle.com/dsv/11895299>

The CSV is currently located at `data/raw/sales_data.csv`. Keep this original file unchanged. The figures below are preliminary figures reported in the proposal's source document; they have not yet been independently verified against the current CSV.

### 5.1 Dataset profile

| Attribute | Proposal-reported details | Verification status |
|---|---:|---|
| Number of records | 76,000 | To verify |
| Number of columns | 16 | To verify |
| Date range | 1 January 2022–30 January 2024 | To verify |
| Stores | 5 | To verify |
| Products | 20 | To verify |
| Product categories | 5 | To verify |
| Regions | 4 | To verify |
| Missing values in initial inspection | 0 | To verify |
| Exact duplicate rows in initial inspection | 0 | To verify |

These are preliminary profiling results. Additional validation is required before the analysis is finalised.

### 5.2 Dataset fields

| Field | Proposal-reported description |
|---|---|
| Date | Date associated with the record |
| Store ID | Store identifier |
| Product ID | Product identifier |
| Category | Product category |
| Region | Store or sales region |
| Inventory Level | Recorded inventory quantity |
| Units Sold | Number of units sold |
| Units Ordered | Number of units ordered |
| Price | Recorded product price |
| Discount | Recorded discount value |
| Weather Condition | Recorded weather category |
| Promotion | Indicator of promotional activity |
| Competitor Pricing | Recorded competitor price |
| Seasonality | Seasonal classification |
| Epidemic | Indicator for the recorded epidemic variable |
| Demand | Recorded demand value |

The exact meaning, units, and business interpretation of each field will be checked against the dataset documentation where available.

## 6. Project Scope

### 6.1 Included in scope

- Dataset profiling and validation.
- Data cleaning and preparation in Excel.
- Excel formulas, PivotTables, and charts.
- Demand and sales analysis.
- Inventory-level and ordering analysis.
- Product, category, store, regional, and time-based comparisons.
- Analysis of recorded discounts, promotions, prices, and contextual variables.
- KPI development.
- Basic demand forecasting, if appropriate.
- Interactive Power BI dashboard development.
- Business insights and recommendations.
- Technical documentation and GitHub publication.

### 6.2 Outside the current scope

The project will not attempt to implement a live inventory management system, connect to a live ERP platform, automate purchase orders, or deploy a production forecasting service.

Python, SQL, and advanced machine learning are excluded from the current two-week implementation. They may be explored in future versions.

## 7. Methodology

The project will follow a structured data analytics workflow.

### Stage 1: Data collection and understanding

- Obtain the selected CSV dataset.
- Record the source and any applicable usage or redistribution restrictions.
- Review the dataset documentation.
- Identify the available fields, data types, and analytical opportunities.

### Stage 2: Data quality assessment

- Check for missing values and duplicate records.
- Validate date formats and date ranges.
- Inspect numerical fields for invalid or unexpected values.
- Check categorical consistency and unexpected labels.
- Investigate unusual values and potential outliers.
- Confirm the expected record grain, such as date, store, and product.

### Stage 3: Data cleaning and preparation

Microsoft Excel will be used to:

- Convert dates and numerical fields to appropriate data types.
- Standardise column names and categorical values where necessary.
- Document any corrections or exclusions.
- Create calculated fields where justified.
- Preserve the original raw dataset.
- Save the cleaned dataset separately.

Changes will be documented so the process can be reviewed and reproduced.

### Stage 4: Exploratory data analysis

The analysis will use Excel formulas, PivotTables, and charts to investigate:

- Demand trends over time.
- Units sold by product and category.
- Demand by store and region.
- Inventory-level distributions.
- Ordering patterns.
- Differences between demand and units sold.
- Patterns associated with promotions, discounts, prices, and seasonality.

Associations will be described as patterns rather than proof of causation.

### Stage 5: KPI development

Relevant KPIs will be calculated using verified fields and documented definitions. Every KPI will be checked for correct aggregation and interpretation before being used in the dashboard.

### Stage 6: Forecasting exploration

If the date and demand data support a reliable time-series analysis, Excel forecasting methods such as moving averages or `FORECAST.ETS` may be explored.

Where forecasting is included, the project will use a time-based validation approach and report an appropriate error measure. Forecast accuracy will not be claimed without comparing predictions with actual observations.

### Stage 7: Power BI dashboard

The cleaned data will be imported into Power BI. Suitable measures, visualisations, filters, and interactions will be created to support the main analytical questions.

### Stage 8: Reporting and publication

The final findings will be summarised in project documentation and the README. Dashboard screenshots and appropriate supporting files will be organised for publication on GitHub, subject to dataset licence terms.

## 8. Data Quality and Validation

Data quality will be assessed before drawing conclusions. The following checks will be included:

- **Completeness:** Verify missing values in relevant fields.
- **Uniqueness:** Check for duplicate records and duplicate date-store-product combinations.
- **Validity:** Verify that dates, identifiers, and numeric values conform to expected formats.
- **Consistency:** Investigate inconsistent categories, labels, or units.
- **Plausibility:** Review unusually high or low values.
- **Aggregation:** Confirm that totals and averages are calculated at the correct level.
- **Reconciliation:** Compare selected Excel calculations with corresponding Power BI results.

An initial check in the source proposal reported no missing values or exact duplicate rows. This does not guarantee that the dataset contains no data quality issues; additional validation is required.

## 9. Key Performance Indicators

The following KPIs are proposed, subject to validation of their definitions and suitability.

| KPI | Definition or calculation | Purpose |
|---|---|---|
| Total Units Sold | Sum of Units Sold | Measure recorded sales volume |
| Total Recorded Demand | Sum of Demand | Measure demand recorded in the dataset |
| Average Recorded Demand | Average of Demand at the record level | Summarise recorded demand |
| Total Units Ordered | Sum of Units Ordered | Summarise ordering activity |
| Average Inventory Level | Average of Inventory Level | Examine recorded inventory levels |
| Zero-Inventory Record Rate | Records with Inventory Level = 0 ÷ eligible records | Identify records with no recorded inventory |
| Demand–Sales Difference | Demand minus Units Sold, reported with a clear definition | Examine differences between recorded demand and sales |
| Product Demand Contribution | Product demand ÷ total demand | Compare product contributions |
| Demand Change Over Time | Change in demand between comparable periods | Examine demand trends |
| Forecast Error | Mean absolute error, if forecasting is implemented | Evaluate forecast performance |

### KPI interpretation rules

- A zero-inventory record is not automatically proof of a stockout.
- Demand minus units sold is an analytical difference, not a confirmed measure of lost sales.
- Total units ordered does not necessarily equal replenishment received.
- Inventory turnover requires suitable cost-of-goods-sold and average inventory valuation data; it will not be reported unless those inputs can be validated.
- Reorder risk, supplier lead time, and stockout rates will only be calculated if the required definitions and supporting fields are available.

## 10. Analysis and Dashboard Requirements

The Power BI dashboard will focus on clear business questions.

### 10.1 Overview page

Potential visuals:

- Total units sold.
- Total recorded demand.
- Total units ordered.
- Average recorded inventory level.
- Demand trend over time.
- Demand by category and region.

### 10.2 Demand and product analysis

Potential visuals:

- Demand over time.
- Demand by product and category.
- Product contribution to total demand.
- Store and regional comparisons.
- Seasonal demand comparisons.

### 10.3 Inventory and ordering analysis

Potential visuals:

- Inventory-level trends.
- Distribution of inventory levels.
- Records with zero inventory.
- Units ordered compared with units sold.
- Demand and sales differences, clearly labelled.

### 10.4 Business factors

Potential visuals:

- Demand across promotion and non-promotion records.
- Demand patterns by discount band.
- Recorded demand by weather condition.
- Demand by season.
- Product price and competitor price comparisons.

These comparisons will be interpreted carefully. They will not establish that promotions, weather, or pricing caused a change in demand.

### 10.5 Interactivity

Where supported by the data model, the dashboard will include filters for:

- Date.
- Store.
- Product.
- Category.
- Region.

The final dashboard will prioritise clarity and usefulness rather than including every possible chart.

## 11. Project Deliverables

The completed project is expected to include:

- Original dataset, retained separately and handled in accordance with its licence.
- Cleaned and validated dataset.
- Excel analysis workbook with calculations, PivotTables, and charts.
- Data quality findings and data documentation.
- Power BI dashboard file.
- Dashboard preview image.
- Evidence-based business insights and recommendations documented in the README.
- Updated project proposal and project management tracker.
- GitHub README with project overview, tools, methodology, KPIs, and findings.
- Final project review and reflection.

## 12. Project Management Plan (PM-01 to PM-14)

The project is planned over two weeks, with seven tasks per week.

| ID | Task | Planned timing | Expected output |
|---|---|---|---|
| PM-01 | Confirm scope and project plan | Week 1, Day 1 | Approved project scope |
| PM-02 | Source and document dataset | Week 1, Day 1 | Raw dataset and source record |
| PM-03 | Profile dataset and inspect fields | Week 1, Day 2 | Initial data quality findings |
| PM-04 | Clean and prepare data in Excel | Week 1, Days 2–3 | Cleaned dataset |
| PM-05 | Validate data and calculations | Week 1, Day 3 | Validation checklist |
| PM-06 | Create Excel calculations and PivotTables | Week 1, Days 4–5 | Analysis workbook |
| PM-07 | Complete exploratory analysis | Week 1, Days 5–7 | Initial analytical findings |
| PM-08 | Compare products, stores, regions, and periods | Week 2, Day 8 | Comparative analysis |
| PM-09 | Define and validate KPIs | Week 2, Day 8 | KPI reference sheet |
| PM-10 | Build Power BI dashboard | Week 2, Days 9–10 | Interactive dashboard |
| PM-11 | Interpret results and prepare recommendations | Week 2, Day 11 | Business insights |
| PM-12 | Complete project documentation | Week 2, Day 12 | Project documents |
| PM-13 | Organise and publish GitHub repository | Week 2, Day 13 | Published portfolio repository |
| PM-14 | Review, test, and finalise project | Week 2, Day 14 | Final quality-checked project |

Task durations are planning estimates. If data quality issues or dashboard development take longer than expected, scope will be prioritised to preserve the two-week deadline. Git commits will be recorded as work is completed, rather than waiting until the final day.

## 13. Expected Outcomes

By the end of the project, I expect to demonstrate that I can:

- Assess and prepare a moderately sized business dataset.
- Use Excel to clean, validate, analyse, and summarise data.
- Define and calculate business KPIs accurately.
- Analyse demand, inventory indicators, and ordering activity.
- Build an interactive Power BI dashboard.
- Communicate findings in business-friendly language.
- Document an analytics workflow professionally.
- Maintain a structured GitHub portfolio repository.

The findings will be based on the actual dataset and will not be assumed in advance.

## 14. Limitations and Assumptions

- The dataset is not confirmed to represent a specific real-world retailer or operational system.
- The meaning and business context of some variables may require further documentation.
- Recorded inventory levels may not establish whether a stockout occurred throughout a day.
- Units ordered may not represent units received.
- Supplier lead time, replenishment dates, and cost of goods sold are not among the identified columns.
- Forecasting performance depends on the quality, consistency, and historical depth of the demand series.
- Relationships between demand and external factors will not be interpreted as causal without appropriate evidence.
- Findings may not generalise to every retailer or supply chain.

The project will document these limitations and avoid presenting unsupported conclusions.

## 15. Future Development

Possible future improvements include:

- Rebuilding the analysis with SQL and Python.
- Comparing multiple forecasting methods.
- Evaluating forecasts with a dedicated holdout period.
- Creating a more detailed inventory replenishment model if suitable data becomes available.
- Adding supplier lead-time and stockout data.
- Exploring inventory optimisation and reorder-point calculations.
- Developing an automated data refresh process.
- Comparing findings across additional datasets.

These enhancements are outside the current two-week scope and will be considered after the first version is completed.

## 16. Conclusion

The Inventory & Demand Analysis project will provide a structured opportunity to develop practical skills in Excel, Power BI, data validation, KPI development, demand analysis, and business reporting.

Using the selected retail dataset, I will work through the complete analytical process, from raw data inspection to an interactive dashboard and documented business insights.

The final project will be published as a professional portfolio example supporting my progression towards Data Analyst, Inventory Analyst, Supply Chain Analyst, and ultimately Data Scientist roles.

## Professional project principles

- Keep the original CSV unchanged and save any cleaned version separately.
- Record each PM-01 to PM-14 task with status, completion date, issues, and Git commit.
- Validate each KPI before building the dashboard.
- Do not claim stockouts, lost sales, or inventory turnover unless the available data supports those measures.
