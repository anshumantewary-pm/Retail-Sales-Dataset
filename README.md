# Retail Sales Analysis: Excel and Power BI

A business intelligence project on a multi-category retail dataset (5,000 transactions, five stores, four regions). The raw transaction, product, customer and store tables were cleaned and joined in Excel with VLOOKUP, summarised with pivot tables and an Excel dashboard, and then explored in an interactive Power BI report. The written report explains the BI framework, the KPIs used, each dashboard page, and the findings and recommendations. It was prepared as the CA1 assignment for the Business Analytics II course (MKTM504).

## Dataset

- 5,000 transactions × 25 columns, dated September 2023 to September 2025
- Separate **Transactions**, **Products** (50), **Customers** (200) and **Stores** (5) tables, joined into one accumulated table
- Categories: Electronics, Fashion, Groceries · Regions: East, North, South, West
- Payment methods: Cash, Credit Card, Bank Transfer, Mobile Money

## Approach

1. **Data cleaning in Excel:** duplicate check on TransactionID, `COUNTBLANK` missing-value audit, data-type and currency formatting, outlier checks (Sales ≈ Quantity × UnitPrice × (1 − Discount)), and region/store and category/sub-category consistency checks with `COUNTIF`
2. **Data modelling:** `VLOOKUP` (wrapped in `IFERROR`) to bring product, customer and store attributes into the transaction table
3. **Pivot analysis:** sales by category × region, and profit and margin by category
4. **Excel dashboard:** KPI cards (sales, quantity, profit), charts and slicers
5. **Power BI report** (described in the report): Home page with bookmark navigation, KPI dashboard, month-wise trends, decomposition tree (Region → Category → Product → Store) and a table/matrix page with conditional formatting, slicers, drill-through and cross-filtering

## Key findings (from the report and workbook)

| KPI | Value |
| --- | --- |
| Total sales | ₹14.30M |
| Total profit | ₹1.67M |
| Units sold | 14,949 |
| Net profit margin | 11.7% |

| Category | Sales | Profit | Margin |
| --- | --- | --- | --- |
| Electronics | ₹6.32M | ₹713.7K | 11.3% |
| Fashion | ₹6.23M | ₹729.3K | 11.7% |
| Groceries | ₹1.75M | ₹230.1K | 13.1% |

- **East leads:** ₹5.60M, or 39.2% of sales; West (₹2.92M), North (₹2.90M) and South (₹2.88M) are close to each other
- **Growth:** sales rose from ₹2.18M in 2023 to ₹7.03M in 2024 (+222%), and the partial 2025 year reached ₹5.10M. The data starts in September 2023, so part of that jump reflects a shorter first year
- **Category mix is stable:** about 44% Electronics, 44% Fashion and 12% Groceries in every month, with no clear seasonal spike
- **Payments are evenly split:** Cash ₹3.68M, Credit Card ₹3.67M, Mobile Money ₹3.56M, Bank Transfer ₹3.39M
- **Top 5 products** (Book Television, And Footwear, Set Dairy, Traditional Laptop, Beat Accessories) make up about 19.4% of sales
- **Opportunities:** South Fashion (₹1.14M against ₹2.50M in the East) and low-selling SKUs such as "Difficult Vegetables" (₹20,126, sold in a single store)

The report recommends copying what works in the East to other regions, a targeted Fashion push in the South, deeper grocery ranges, and reviewing the weakest SKUs.

## Tools & tech

Microsoft Excel (VLOOKUP, COUNTIF, COUNTBLANK, pivot tables, slicers, charts) · Power BI (DAX measures, bookmarks, decomposition tree, drill-through, conditional formatting)

## Repository structure

```
├── Retail Sales Data Excel Dashboard.xlsx   # source tables, accumulated data, pivots and dashboard
├── Report of Retail Dataset.pdf             # 21-page written report with dashboard screenshots
├── Anshuman Tewary Blinkit.pbix             # Power BI dashboard on BlinkIT grocery data
└── LICENSE
```

## How to open

- **Excel:** open `Retail Sales Data Excel Dashboard.xlsx`. The `Dashboard` and `Pivot` sheets hold the summaries, and the raw tables are on the other sheets.
- **Report:** open [`Report of Retail Dataset.pdf`](Report%20of%20Retail%20Dataset.pdf) for the full write-up and screenshots of the Power BI report pages.
- **Power BI:** open `Anshuman Tewary Blinkit.pbix` in Power BI Desktop.

> Note: the `.pbix` in this repo is built on a separate BlinkIT grocery dataset (item type, outlet type, fat content, ratings). The five-page Power BI report for the retail dataset is documented through screenshots in the PDF.

## License

Released under the [MIT License](LICENSE).

---

Anshuman Tewary · [GitHub](https://github.com/anshumantewary-pm) · [LinkedIn](https://www.linkedin.com/in/tewary-anshuman/)
