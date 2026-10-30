![Dashboard](Documents/Dashboard.png)
# Retail Sales Analysis

An Excel-based analysis of 1,000 retail transactions (January 2023 – January 2024) covering overall sales performance, customer purchasing behavior, product performance and monthly sales trends. The goal is to support data-driven business decisions.

## Business Questions

1. How much revenue are we generating?
2. How many products are we selling?
3. What is the average value of each transaction?
4. Which product category generates the most revenue?
5. Who are our customers (age and gender)?
6. Are sales increasing or decreasing over time?

## Key Results

| Metric | Result |
|---|---|
| Total revenue (sum of Total Amount) | **$456,000** |
| Total quantity sold | **2,514 units** |
| Number of transactions | 1,000 |
| Average order value (AOV) | **$456.00** (median $135) |
| Top category by revenue | **Electronics** – $156,905 (34.4%) |
| Customer gender split | 51.0% female / 49.0% male |
| Average customer age | 41.4 years (range 18–64) |
| Sales trend | Flat with high month-to-month volatility |

## Highlights

- **High-ticket items drive revenue.** Products priced at $300 and $500 make up 39.6% of orders but 88.4% of revenue.
- **Categories are near-equal.** Electronics ($156,905), Clothing ($155,580) and Beauty ($143,515) are separated by only 2.9% of total revenue.
- **Younger customers spend more per order.** AOV is $500 for ages 18–25 versus $412 for ages 56–64. The 46–55 group contributes the most total revenue.
- **No clear growth or decline.** Monthly revenue ranges from $23.6K (September) to $53.2K (May) around an average of about $37.9K. Second-half 2023 revenue was 4.3% lower than first-half.
- **No repeat customers.** All 1,000 Customer IDs are unique, so retention is the largest untapped growth opportunity.

## Dataset

| Field | Description |
|---|---|
| Transaction ID | Unique transaction identifier (1–1,000) |
| Date | Transaction date |
| Customer ID | Unique customer identifier |
| Gender | Male or Female |
| Age | Customer age (18–64) |
| Product Category | Beauty, Clothing or Electronics |
| Quantity | Units purchased (1–4) |
| Price per Unit | $25, $30, $50, $300 or $500 |
| Total Amount | Quantity × Price per Unit |

**Data quality checks:** no missing values, no duplicate IDs, and Quantity × Price per Unit equals Total Amount on every row. January 2024 contains only 2 transactions, so it is included in overall totals but excluded from monthly trend conclusions.

## Methodology

All analysis was done in **Microsoft Excel**:

- **Totals and AOV:** `SUM` on Total Amount and Quantity; AOV = total revenue ÷ number of transactions
- **Category, gender and age breakdowns:** PivotTables and `SUMIFS` / `COUNTIFS`
- **Age groups:** helper column using `IFS` with bands 18–25, 26–35, 36–45, 46–55 and 56–64
- **Monthly trend:** PivotTable with dates grouped by month

## Repository Contents

| File | Description |
|---|---|
| `Retail_Sales_Analysis_Report.pdf` | Full written report with findings, charts, answers to the business questions, recommendations and limitations |
| Excel workbook (analysis and dashboard) | Data, PivotTables, calculations and interactive dashboard |
| `README.md` | Project overview |

## Recommendations

1. Protect and grow the high-ticket ($300 and $500) product mix.
2. Treat the three categories as a balanced portfolio: lift Beauty order volume and upsell Clothing.
3. Target marketing by age: premium and Beauty offers for 18–25, Electronics-led loyalty for 46–55, premium bundles for 56–64.
4. Plan promotions around weak months (March, April, July, September, November) and stock for peaks (February, May, October, December).
5. Build a repeat-purchase programme to turn one-time buyers into returning customers.
6. Use broad campaigns across genders, personalising only by category affinity.

## Limitations

- Only one year of data, so seasonality cannot be validated against prior years.
- No cost or margin data, so conclusions reflect revenue rather than profit.
- Each customer appears once, so repeat behavior and lifetime value cannot be measured.
- Age groups are analyst-defined; other bands may shift segment-level results slightly.

## Tools

Microsoft Excel (formulas, PivotTables, dashboard).
