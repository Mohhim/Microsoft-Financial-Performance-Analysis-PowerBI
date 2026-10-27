# Microsoft-Financial-Performance-Analysis-PowerBI
Microsoft financial performance analysis using Power BI, DAX, and financial reporting data (FY2023–FY2025).
[README.md](https://github.com/user-attachments/files/34009595/README.md)
# Microsoft Financial Performance Analysis | Power BI

An interactive Power BI portfolio project analyzing **Microsoft's financial performance across FY2023–FY2025**, using figures from published annual financial statements. The report focuses on profitability, business segments, growth, cash generation, and capital expenditure.

> **Scope:** Historical FY2023–FY2025 analysis. This is an independent educational portfolio project, not an official Microsoft dashboard or an assessment of FY2026 results.

## Project objectives

- Track revenue, operating income, net income, and profitability margins.
- Compare year-over-year performance across fiscal years.
- Analyze Microsoft's three reported business segments.
- Assess operating cash flow, capital expenditure (CapEx), free cash flow (FCF), and cash conversion.
- Present decision-ready financial insights through interactive Power BI dashboards.

## Dashboard pages

### 1. Executive Overview
Executive KPIs, financial trends, margin trends, and revenue contribution by business segment.

### 2. Revenue & Profitability Analysis
Revenue, gross profit, net income, year-over-year revenue growth, and net profit margin.

### 3. Business Segment Analysis
Revenue trends, operating margins, year-over-year segment growth, and identification of the fastest-growing segment.

### 4. Cash Flow Analysis
Operating cash flow, capital expenditure, free cash flow, and cash conversion trends.

## Key findings

| Metric | FY2023 | FY2024 | FY2025 |
|---|---:|---:|---:|
| Revenue (USD B) | 211.92 | 245.12 | 281.72 |
| Operating income (USD B) | 88.52 | 109.43 | 128.53 |
| Net income (USD B) | 72.36 | 88.14 | 101.83 |
| Operating cash flow (USD B) | 87.58 | 118.55 | 136.16 |
| Free cash flow (USD B) | 59.48 | 74.07 | 71.61 |

- Revenue increased **32.94%** between FY2023 and FY2025.
- FY2025 revenue growth was **14.93%** year over year.
- **Intelligent Cloud** was the fastest-growing business segment in FY2025, with approximately **21.50%** year-over-year revenue growth.
- FY2025 operating cash flow reached **$136.16B**, while CapEx reached **$64.55B**.
- FY2025 free cash flow was **$71.61B**, approximately **3.32% lower** than FY2024.

*Financial values are rounded for presentation. USD B = billions of US dollars. Fiscal years end June 30.*

## Tools and techniques

- **Power BI Desktop** — data modeling, report design, interactive visuals
- **Power Query** — data import and preparation
- **DAX** — financial KPIs, ratios, growth rates, and year-over-year comparisons
- **Star-schema modeling** — shared fiscal-year dimension connected to financial fact tables
- **Financial analysis** — income statement, segment performance, and cash flow analysis

## Data model

The model uses a fiscal-year dimension and three financial fact tables:

- `Dim_FiscalYear`
- `Fact_IncomeStatement`
- `Fact_Segments`
- `Fact_CashFlow`

Financial source values are stored in **USD millions**; selected measures are converted to **USD billions** for dashboard display.

## Screenshots

Screenshots will be added here after exporting the final report pages from Power BI Desktop.

## How to explore the project

1. Download the `.pbix` file from this repository once uploaded.
2. Open it with **Microsoft Power BI Desktop**.
3. Navigate across the four analytical dashboard pages.
4. Use the fiscal-year slicer to explore year-specific KPIs; multi-year trend visuals are designed to retain historical context.

> **Refresh note:** If the report uses local CSV or Excel files, Power BI may require updating their file paths before refreshing on another computer. Include the source data files in the repository only after confirming they are suitable for redistribution.

## Data sources

Financial figures are based on Microsoft's publicly reported annual results:

- [Microsoft FY2025 Form 10-K — SEC](https://www.sec.gov/Archives/edgar/data/789019/000095017025100235/msft-20250630.htm) — FY2025, FY2024, and FY2023 financial statements and segment disclosures.
- [Microsoft FY2024 Form 10-K — SEC](https://www.sec.gov/Archives/edgar/data/789019/000095017024087843/msft-20240630.htm) — additional comparative financial information.

**Disclaimer:** This project is independently prepared for educational and portfolio purposes. It is not affiliated with or endorsed by Microsoft. Historical financial information does not constitute investment advice.
