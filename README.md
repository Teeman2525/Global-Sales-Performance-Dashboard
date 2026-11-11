# Global Sales Performance Dashboard | Excel Portfolio Project

An interactive **Microsoft Excel sales analytics dashboard** covering **2015–2022**, designed to help stakeholders explore revenue, profitability, orders, regional performance, sales channels, and product categories.

![Global Sales Performance Dashboard](Excel%20Dashboard.jpg)

## Project overview

The goal was to turn sales records into a clear, filterable business-performance dashboard while documenting data-quality uncertainties. The dashboard uses **Year** and **Country** slicers; both update the four charts **and** four KPI cards.

## Key performance indicators

| KPI | All-record value | Calculation |
|---|---:|---|
| Total Revenue | **$6.63B** | Sum of Total Revenue |
| Total Profit | **$1.96B** | Sum of Total Profit |
| Profit Margin | **29.62%** | Total Profit ÷ Total Revenue |
| Total Orders | **5,000** | Count of unique, nonblank Order IDs |

*Values shown are for all 5,000 records with filters cleared; they change when dashboard slicers are used.*

## Dashboard features

- **Monthly revenue line chart:** January–December totals aggregated across 2015–2022 (not a continuous monthly time series).
- **Revenue by region:** Horizontal bar chart comparing geographic contributions.
- **Sales-channel revenue share:** Online vs. offline donut chart.
- **Profit by item type:** Ranked horizontal bar chart.
- **Interactive slicers:** Year and Country control all charts and KPI cards.
- **Consistent design:** Navy, teal, and light-blue palette with readable KPI cards and axis formats.

## Tools and techniques

**Microsoft Excel** · Excel Tables and structured references · PivotTables · PivotCharts · SUM / COUNTA / TEXT / IFERROR · slicer report connections · dynamic KPI display cells · dashboard design · data-quality checks.

A dedicated KPI PivotTable supplies filtered revenue, profit, and order count; the profit-margin card divides filtered profit by filtered revenue.

## Key findings and recommendations

| Finding | Recommended next step |
|---|---|
| January has the highest aggregated calendar-month revenue; September the lowest. | Check individual years before claiming a recurring seasonal pattern; investigate demand and campaign differences. |
| Sub-Saharan Africa leads regional revenue; Europe follows. | Compare regional profit, margins, costs, and product mix before deciding where to invest. |
| Offline contributes about **51%** of revenue and online about **49%**. | Compare channel profitability, acquisition cost, retention, and customer value; revenue share alone is not enough. |
| Cosmetics generates the highest total profit (about **$372.41M**). | Evaluate category margins, sales volumes, cost structure, and growth rather than prioritizing solely by total profit. |

## Data-quality decisions and limitations

- **1,174 records** are labelled `Cancelled` in **Order Priority**, *not* in a verified transaction-status field. They were **retained** because their business meaning is unconfirmed; they should not automatically be treated as refunds or invalid sales.
- **203 records** have a Ship Date earlier than Order Date. They were flagged, not silently removed.
- **5,000 Order IDs** were checked as unique.
- The source's `Total Profit` measure may not account for all operating costs; complete accounting profitability was not verified.
- The monthly chart groups like months across eight years; it cannot establish year-by-year seasonality by itself.

## Repository structure

```text
Global-Sales-Performance-Dashboard/
├── README.md
├── GSPP.xlsx                       # Interactive Excel dashboard (add your workbook)
├── Excel Dashboard.jpg             # Dashboard preview
└── Global_Sales_Performance_Case_Study.docx
```

## How to explore

1. Open `GSPP.xlsx` in desktop Microsoft Excel.
2. Go to the **Portfolio Dashboard** sheet.
3. Use the **Year** and **Country** slicers to explore the KPIs and charts.
4. Clear the slicers to restore the full dataset.

## What I learned

This project strengthened my ability to build interactive Excel dashboards, connect PivotTables through slicers, create filter-responsive KPIs, distinguish revenue from profitability, and communicate data limitations without making unsupported assumptions.

## Future improvements

Validate ambiguous status fields with a data owner; investigate shipping-date anomalies; analyze year-over-year growth and category margins; and enrich channel analysis with CRM and operating-cost data.
