[README_PROFESSIONAL.md](https://github.com/user-attachments/files/34015502/README_PROFESSIONAL.md)
# Microsoft Financial Performance Analysis | Power BI

**An executive-style Power BI portfolio project analyzing Microsoft’s FY2023–FY2025 financial performance across profitability, business segments, and cash flow.**

> **Independent portfolio project.** Not affiliated with or endorsed by Microsoft. Financial figures are based on publicly reported company results; this dashboard is for analytical demonstration, not investment advice. Fiscal years refer to Microsoft’s reporting years, not calendar years.

## Project at a Glance

| | |
|---|---|
| **Period** | FY2023–FY2025 |
| **Tool** | Microsoft Power BI Desktop |
| **Data** | Financial statements, business segment results, cash flow |
| **Model** | Fiscal-year dimension connected to three fact tables |
| **Deliverable** | Four interactive report pages and a Power BI (`.pbix`) file |

## Business Questions

This report was designed to answer five executive-level questions:

1. How have revenue, operating income, and net income changed across the three fiscal years?
2. Are profitability margins improving alongside revenue growth?
3. Which business segments contribute the most revenue and show the strongest growth?
4. How are operating cash flow and capital expenditures evolving?
5. Is free cash flow keeping pace with operating cash generation?

## Dashboard Gallery

### 1. Executive Overview

Financial KPIs, revenue and income trends, margin trends, and business segment contribution.

![Executive Overview dashboard](Screenshots/Executive_Overview.PNG)

### 2. Revenue & Profitability Analysis

Revenue growth, gross profit, net income, and profitability trends across FY2023–FY2025.

![Revenue and Profitability dashboard](Screenshots/Revenue_Profitability.PNG)

### 3. Business Segment Analysis

Segment-level revenue, operating margins, year-over-year growth, and multi-year performance.

![Business Segment Analysis dashboard](Screenshots/Business_Segments.PNG)

### 4. Cash Flow Analysis

Operating cash flow, capital expenditure, free cash flow, and cash conversion trends.

![Cash Flow Analysis dashboard](Screenshots/Cash_Flow.PNG)

### 5. Data Model

![Power BI relationship model](Screenshots/Data_Model.PNG)

## Selected Financial Insights

| Metric | FY2025 result |
|---|---:|
| Revenue | **$281.72B** |
| Operating income | **$128.53B** |
| Net income | **$101.83B** |
| Net profit margin | **36.15%** |
| Operating cash flow | **$136.16B** |
| Capital expenditure | **$64.55B** |
| Free cash flow | **$71.61B** |

- **Revenue expansion:** Revenue increased from **$211.92B in FY2023** to **$281.72B in FY2025** (approximately **32.94%** over the period).
- **Profitability:** Operating margin increased from approximately **41.77%** in FY2023 to **45.62%** in FY2025, an increase of about **3.85 percentage points**.
- **Segment momentum:** Intelligent Cloud recorded approximately **21.50%** year-over-year revenue growth in FY2025, the fastest among the three reported segments.
- **Cash flow trade-off:** FY2025 operating cash flow reached **$136.16B**, while capital expenditure reached **$64.55B**. Free cash flow was **$71.61B**, approximately **3.32% lower** than FY2024.

**Units:** Underlying CSV financial values are expressed in **USD millions**; headline dashboard KPIs are shown in **USD billions**. Percentages are rounded.

## Data & Modeling Approach

The project uses a simple analytical model with a shared fiscal-year dimension:

- `Dim_FiscalYear` — fiscal-year lookup table.
- `Fact_IncomeStatement` — income statement metrics by fiscal year.
- `Fact_Segments` — business segment revenue, costs, and operating income.
- `Fact_CashFlow` — operating, investing, and financing cash flow metrics, including capital expenditure.

The fiscal-year dimension has **one-to-many, single-direction relationships** to the three fact tables. Financial measures are calculated using DAX rather than relying on raw totals in every visual.

### Key calculations

| KPI | Business definition |
|---|---|
| Gross profit margin | Gross profit / revenue |
| Operating margin | Operating income / revenue |
| Net profit margin | Net income / revenue |
| Revenue YoY growth | (Current-year revenue − prior-year revenue) / prior-year revenue |
| Segment operating margin | Segment operating income / segment revenue |
| Free cash flow | Operating cash flow − capital expenditure |
| Cash conversion ratio | Operating cash flow / net income |

The first available fiscal year has no preceding year in the dataset, so year-over-year measures for FY2023 are intentionally blank.

### Report interaction design

The fiscal-year slicer filters relevant KPI cards and segment comparisons. Multi-year trend charts retain the FY2023–FY2025 context, enabling comparisons without losing historical trends. Two internal validation pages were used during development and are hidden from normal report navigation.

## Tools & Skills Demonstrated

**Power BI Desktop · Power Query · Star-schema modeling · DAX · Financial KPI analysis · YoY comparisons · Data visualization · Executive reporting**

## Repository Structure

```text
Microsoft-Financial-Performance-Analysis-PowerBI/
├── README.md
├── Microsoft_Financial_Performance_Analysis.pbix
├── Data/
│   ├── README.md
│   ├── cash_flow.csv
│   ├── fiscal_years.csv
│   ├── income_statement.csv
│   └── segments.csv
└── Screenshots/
    ├── README.md
    ├── Executive_Overview.PNG
    ├── Revenue_Profitability.PNG
    ├── Business_Segments.PNG
    ├── Cash_Flow.PNG
    └── Data_Model.PNG
```

## How to Run

1. Download the [Power BI report](Microsoft_Financial_Performance_Analysis.pbix) and the files in the [`Data`](Data/) folder.
2. Open the `.pbix` file in **Power BI Desktop**.
3. If prompted about file locations, update the Power Query data source paths to the downloaded CSV files.
4. Select **Refresh** and explore the four visible report pages.
5. Change the fiscal-year slicer to compare selected-year metrics; use the trend charts for multi-year context.

## Data Provenance & Limitations

The CSV tables organize publicly reported Microsoft financial data for **FY2023–FY2025** into an analysis-friendly structure. The data is **not a Microsoft-provided Power BI dataset**, and this repository does not represent an official Microsoft reporting product.

Official reference points:

- [Microsoft Investor Relations — Annual Reports](https://www.microsoft.com/en-us/Investor/annual-reports.aspx)
- [Microsoft Investor Relations](https://www.microsoft.com/en-us/Investor/)

**Interpretation notes:** The analysis covers three annual observations only, uses rounded display values, and does not include balance-sheet ratios, market valuation, or forward-looking forecasts. Year-over-year comparisons should be interpreted within that scope.

## Author

**[Mohhim](https://github.com/Mohhim)** — Data Analytics & Business Intelligence Portfolio
