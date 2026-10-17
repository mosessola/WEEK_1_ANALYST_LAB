# WEEK_1_ANALYST_LAB
# ShopSmart Retail Analysis – Week 1 (Data Analytics Track)

**Programme:** AnalystLab Africa Experience Lab · **Mission 01:** Retail Sales Analysis with Microsoft Excel
**Client:** ShopSmart Retail Ltd · **Role:** Junior Data Analyst · **Period analysed:** January–December 2025

## Files

| File | What it contains |
|---|---|
| `ShopSmart_Analysis.xlsx` | Cleaned data (as Excel Tables), formulas, lookups, summaries, charts, business answers |
| `Business_Report.pdf` | One-page report: 3 findings, 3 recommendations, 1 risk, 1 opportunity (Part 9) |
| `Data_Understanding.pdf` | One-page explanation with keys and relationship diagram (Part 1) |
| `Executive_Dashboard.pdf` | 
## Workbook map (`ShopSmart_Analysis.xlsx`)

| Sheet | Brief part | Notes |
|---|---|---|
| Assumptions | – | Two switches (discount treatment, orders counted), definitions, sensitivity table |
| KPI_Formulas | Part 3 | The ten required metrics, all live formulas |
| Lookups | Part 4 | Type an Order_ID, get customer, store, product, category, brand, price, supplier (VLOOKUP) |
| Business_Questions | Part 8 | Ten questions, answers are live formulas, plus supporting tables |
| Charts | Part 6 | Monthly trend, category, store, top products, region, return rate by category |
| Pivot_Tables, Pivot_Brand | Part 5 | Month, store, category, brand, state, gender, membership, top/bottom 10 products, top 10 customers |
| Cleaning_Log, Flagged_Records | Part 2 | Original cleaning log and flagged records, kept unchanged |
| Customers … Suppliers, Data_Dictionary | Parts 2 and 4 | Excel Tables (`tblCustomers`, `tblOrders` …). Green headers are calculated columns added for the analysis |

Part 1 is covered by `Data_Understanding.pdf`.

## Key definitions (change them on the Assumptions sheet)

- **Revenue** = Quantity × Unit_Price × (1 − Discount ÷ 100), completed orders only, shipping excluded.
- **Discount is a percentage.** Values are 0/5/10/15/20, but the source `Line_Total` subtracts them as naira. This is flagged in the cleaning log and quantified in the sensitivity table.
- **Return rate** = returned orders ÷ counted orders (returns logged on cancelled or pending orders are ignored).
- **State and Region** come from the store where the sale happened. Store regions are inconsistent in the source (the 4 Abuja stores sit in 3 regions), so regional results are indicative.
- **Supplier** is inferred as Brand + " Supplies" because Products has no Supplier_ID.

## Known limitations

- The summaries in Pivot_Tables and Pivot_Brand are formula-driven (SUMIFS), not native PivotTable objects. For native PivotTables, select any cell in the Orders table and use Insert → PivotTable. Month, category, brand, store, state, region, gender and membership are all columns in that table.
- All orders fall in 2025 and the data is very evenly spread, so differences between categories, stores and months are modest.
- Data issues found by the cleaning step (return dates before order dates, returns on non-completed orders, duplicate store names, duplicate emails) are flagged, not corrected.
