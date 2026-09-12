# superstore-dashboard-with-Power-bi# Superstore Sales & Profitability Dashboard (Power BI)

An interactive Power BI dashboard analyzing sales, profit, and delivery performance for a Superstore-style retail dataset (2019–2020), with a dedicated sales forecasting page.

**File:** `pro.pbix`

---

## 📊 Overview

| Metric | Value |
|---|---|
| Total Sales | **$1,565,804.32** |
| Total Profit | **$175,262.11** |
| Overall Profit Margin | **11.2%** |
| Total Orders | 3,003 |
| Unique Customers | 773 |
| Unique Products | 1,742 |
| Avg. Delivery Time | ~3.9 days |
| Return Rate | 4.9% (287 of 5,901 line items) |
| Date Range | Jan 2019 – Dec 2020 |

## 🗂️ Dataset

The core fact table is `SuperStore_Sales_Dataset` (5,901 rows), containing order, customer, product, geography, sales, profit, quantity, returns, payment mode, and delivery fields. A supporting `Salesforecast` table (643 rows of daily sales) powers the Forecasting page.

## 📄 Report Pages

**1. Dashboard**
- KPI cards: Total Sales, Sales by Region, Average Delivery Time
- Sales by Sub-Category and by Ship Mode (bar charts)
- Sales & Profit trend by Month/Year (stacked area charts)
- Profit by State (map)
- Sales split by Segment, Region, and Payment Mode (donut charts)
- Region slicer for cross-filtering

**2. Forecasting**
- Historical vs. forecasted daily sales (line charts)
- Average delivery time by State (bar chart)

## 💡 Key Insights

- **Strong year-over-year growth:** Sales rose from **$564,680 in 2019** to **$1,001,125 in 2020**, a **+77% increase**, while profit grew more modestly (**$81,823 → $93,439**, +14%) — margin compressed as the business scaled.
- **Furniture is a margin problem, not a sales problem:** Furniture generated **$451,509** in sales (comparable to Technology's $470,588) but returned only **$10,007 in profit — a 2.2% margin**, versus Technology's **19.2%** and Office Supplies' **11.6%**.
- **Tables are actively losing money:** The Tables sub-category posted **-$11,092 in profit** on $119,294 of sales, the single biggest drag on overall profitability. Bookcases and Supplies were also unprofitable (-$343 and -$1,654 respectively).
- **Technology and Copiers are the profit engines:** Despite modest sales, Copiers converted at an exceptional margin (**$59,736 sales → $42,775 profit, ~72% margin**), and Accessories/Phones also punched above their weight.
- **Regional imbalance:** The **West region** leads on both sales ($522,441) and profit ($67,860), while the **South** trails on sales — but profit-per-dollar-of-sales is fairly consistent across regions, suggesting the West's edge is volume-driven, not efficiency-driven.
- **High-revenue states aren't always profitable:** California and New York top the sales leaderboard, but **Texas (-$14,078), Pennsylvania (-$9,298), Illinois (-$9,555), and Ohio (-$9,339)** are net loss-making states — worth investigating for discounting or fulfillment cost issues.
- **Fulfillment mix:** Standard Class shipping accounts for **58% of sales** ($912,401) and the bulk of profit, while Same Day shipping is a small niche (~6% of sales).
- **Payment behavior:** Cash-on-Delivery (COD) is the leading payment mode by both sales ($667,418) and profit ($82,092), ahead of Online and Card payments.
- **Returns are contained but non-trivial:** A ~4.9% return rate across ~5,900 line items is a reasonable candidate for a dedicated returns-analysis page (by category, region, or customer).

## 🛠️ Tech Stack

- **Power BI Desktop** (.pbix)
- Data model with calculated columns/measures (e.g., `Avgdelivery`) and a forecast table
- Visuals: bar, stacked area, line, donut, map, KPI, and slicer visuals

## 🚀 How to Use

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows only; free).
2. Download `pro.pbix` from this repository.
3. Open the file in Power BI Desktop — no external data connections are required, as the data is embedded in the file.
4. Use the Region slicer and page tabs (**Dashboard** / **Forecasting**) to explore.

> Note: `.pbix` files can only be opened and edited in Power BI Desktop (Windows). Non-Windows users can view a published version via the [Power BI Service](https://powerbi.microsoft.com) if the report is shared/published.

## 📁 Repository Structure

```
├── pro.pbix          # Power BI report file
├── README.md         # Project documentation
```

