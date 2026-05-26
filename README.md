# DataCo Supply Chain Dashboard
### End-to-End Supply Chain Analytics | Excel + Power BI

**Prepared by:** Md. Bakhtiyar Warsi | Data Analyst | May 2026  
**Contact:** bakhtiyarwarsi8@gmail.com | +91-8699888405  
**Tools:** Microsoft Excel | Power Query | Power BI Desktop

---

## Project Stats

| Metric | Value |
|--------|-------|
| Total Rows | 180,519 rows |
| Unique Orders | 66,000 orders |
| Total Columns | 45 (reduced to 39 after cleaning) |
| Markets | USCA, Europe, LATAM, Pacific Asia, Africa |
| Customer Segments | Consumer, Corporate, Home Office |
| Dashboard Pages | 5 interactive pages |
| DAX Measures | 28 measures |

---

## Project Overview

This project is an end-to-end business intelligence solution built on the DataCo Global Supply Chain dataset. Starting from 180,519 rows of raw transactional CSV data, the project delivers a 5-page interactive Power BI dashboard that gives supply chain leadership a single source of truth for monitoring delivery performance, profitability, customer behaviour, and fraud risk across 5 global markets.

The project covers the complete data analytics workflow:

**Raw Data → Excel Cleaning → Power Query Transformation → DAX Modelling → Interactive Dashboard → Business Recommendations**

---

## Business Problem

DataCo Global had no centralised reporting tool. All operational data sat in raw CSV format making it impossible for leadership to monitor KPIs or act on delivery failures in real time. Four core problems were identified and solved:

| # | Problem | Details |
|---|---------|---------|
| 1 | Delivery Reliability | 54.82% of orders at late delivery risk with no visibility into root causes |
| 2 | Profit Erosion | 37.8% of orders are loss-making — aggressive discounting the root cause |
| 3 | Fraud Exposure | 6.18% fraud rate with no geographic or shipping mode breakdown |
| 4 | No Reporting Tool | All data in raw spreadsheets — no real-time visibility for leadership |

---

## Dashboard Pages

### Page 1 — Executive Overview
**KPIs:** $36.8M Total Sales · 66K Orders · $4.0M Profit · 21K Customers · 54.82% Late Delivery · 4,062 Fraud Orders

**Visuals:**
- Line chart: Sales & Profit trend by Month
- Bar chart: Sales by Market
- Donut chart: Order Status breakdown

![Page 1 - Executive Overview](screenshots/page1_overview.png)

---

### Page 2 — Delivery Performance
**KPIs:** 54.82% Late · 45.18% On Time · 0.57 Days Avg Delay · 3,692 Canceled Orders

**Visuals:**
- Stacked bar: Late vs On Time by Shipping Mode
- Clustered bar: Avg Real vs Scheduled Shipping Days by Mode
- Bar chart: Late Delivery % by Order Region
- Slicers: Market, Shipping Mode, Date Range

![Page 2 - Delivery Performance](screenshots/page2_delivery.png)

---

### Page 3 — Profitability & Discounts
**KPIs:** 10.78% Profit Margin · 10.17% Avg Discount · 25K Loss Making Orders · $60.33 Avg Profit/Order

**Visuals:**
- Bar chart: Profit by Category (conditional formatting)
- Bar chart: Profit Margin % by Department
- Scatter chart: Discount Rate vs Profit Ratio with trend line
- Bar chart: Total Orders by Discount Band

![Page 3 - Profitability](screenshots/page3_profitability.png)

---

### Page 4 — Customer Analysis
**KPIs:** $1.78K Avg Sales/Customer · $192.08 Profit/Customer · 3.18 Orders/Customer

**Visuals:**
- Bar chart: Top 10 Customers by Sales
- Map: Customer Locations (bubble size = Total Sales)
- Donut chart: Sales by Customer Segment
- Bar chart: Late Delivery % by Segment

![Page 4 - Customer Analysis](screenshots/page4_customer.png)

---

### Page 5 — Risk & Fraud
**KPIs:** 6.18% Fraud Rate · 4,062 Fraud Orders · 6,532 High Risk Orders · 9,804 On Hold · 5.62% Cancellation Rate

**Visuals:**
- Bar chart: Fraud Orders by Region (conditional formatting)
- Bar chart: Fraud Orders by Shipping Mode
- Line chart: Cancellation Rate % by Month

![Page 5 - Risk & Fraud](screenshots/page5_risk_fraud.png)

---

## Key Findings

| # | Finding | Business Implication |
|---|---------|----------------------|
| 1 | 54.82% Late Delivery Rate | Systemic logistics failure — all 3 segments affected equally (54.73–55.23%). Not a prioritisation issue. |
| 2 | Avg Delay Only 0.57 Days | Most late orders are marginally late. Process improvements could significantly improve on-time rate. |
| 3 | 37.8% Orders Loss-Making | Scatter confirms: discount rate above 10% directly erodes profit ratio. Cap discounts immediately. |
| 4 | Western Europe = Fraud Hub | 705 fraud orders — highest of any region. Standard Class preferred in 2.4K of 4,062 fraud orders. |
| 5 | Consumer = 51% of Revenue | $19.1M from Consumer vs $11.17M Corporate. Corporate offers better margin growth potential. |
| 6 | 9,804 Orders On Hold | Significant stalled revenue — root cause investigation could unlock substantial cash flow. |

---

## Tools & Workflow

| Tool | Phase | What Was Done |
|------|-------|---------------|
| Microsoft Excel | Phase 1 — Cleaning | Removed 6 PII columns. Standardized 5 categorical columns. Fixed data types. Handled nulls. |
| Power Query | Phase 2 — Transform | Added 5 calculated columns: Shipping Delay, Is Late, Order Year, Order Month, Discount Band. |
| Power BI Desktop | Phase 3 — Dashboard | Built data model. Created 28 DAX measures. Delivered 5-page interactive dashboard. |

---

## DAX Measures — 28 Total

| Page | Measures |
|------|----------|
| Page 1 — Overview | Total Sales, Total Orders, Total Profit, Total Customers, Overall Late Delivery %, Fraud Order Count |
| Page 2 — Delivery | Late Delivery Count, On Time Delivery Count, Late Delivery %, On Time Rate %, Avg Shipping Delay (Days), Avg Real Shipping Days, Avg Scheduled Shipping Days, Canceled Orders |
| Page 3 — Profit | Profit Margin %, Avg Discount Rate %, Total Discount Given, Avg Profit Per Order, Avg Order Item Profit Ratio, Loss Making Orders, High Discount Orders |
| Page 4 — Customer | Avg Sales Per Customer, Profit Per Customer, Orders Per Customer, Corporate Segment Sales, Consumer Segment Sales, Home Office Segment Sales |
| Page 5 — Risk | Fraud Rate %, Fraud Orders Count, High Risk Orders, Payment Review Orders, On Hold Orders, Cancellation Rate % |

---

## Challenges & How I Solved Them

| Challenge | Solution |
|-----------|----------|
| Late_delivery_risk stored as True/False boolean causing DAX errors | Replaced TRUE/FALSE with 1/0 in Power Query using Replace Values, changed type to Whole Number |
| 180K rows but only 66K unique orders causing COUNTROWS to overcount | Switched all count measures to DISTINCTCOUNT on Order Id |
| Late Delivery % showing 150%+ due to duplicate row counting | Rewrote Late Delivery Count using DISTINCTCOUNT instead of COUNTROWS |
| Shipping Mode column deleted during Excel cleaning | Retrieved from original source CSV and re-added before reloading into Power BI |

---

## Data Preview

![Cleaned Data Preview](screenshots/cleaned_data_preview.png)
![Column List](screenshots/cleaned_data_columns.png)

> **Note:** Full dataset and .pbix file available on request via email.  
> Contact: bakhtiyarwarsi8@gmail.com

---

## How to Open This Project

**Requirements:** Power BI Desktop (free — [download here](https://powerbi.microsoft.com/desktop)) + DataCo_Cleaned.xlsx

1. Download or clone this repository
2. Open Power BI Desktop
3. Open `DataCo_Supply_Chain_Dashboard.pbix`
4. If prompted, update the data source path to your local `DataCo_Cleaned.xlsx`
5. Click Refresh to load the data
6. Navigate the 5 pages using the tabs at the bottom

---

## Repository Files

| File | Description |
|------|-------------|
| `README.md` | Project documentation — this file |
| `Memo.docx` | Operational analytics memo with findings and recommendations |
| `screenshots/` | Screenshots of all 5 dashboard pages and data preview |

> .pbix and .xlsx files available on request — contact bakhtiyarwarsi8@gmail.com

---

## Recommendations

1. **Standard Class Shipping Review** — Audit carrier performance. Mandate First Class for high-value orders. Expected: 15-20% reduction in late delivery rate.
2. **Discount Cap Policy** — Hard cap of 10% for loss-making categories. Expected: 5-8% improvement in Profit Margin %.
3. **Western Europe Fraud Controls** — Flag Standard Class orders from Western Europe above threshold value. Expected: 25-30% reduction in fraud orders.
4. **Peak Period Capacity Management** — Cap Standard Class volume at 85% capacity during Month 7 surge. Expected: 20-25% reduction in cancellation rate.

---

*Prepared by: Md. Bakhtiyar Warsi | Data Analyst | May 2026*  
*bakhtiyarwarsi8@gmail.com | +91-8699888405*
