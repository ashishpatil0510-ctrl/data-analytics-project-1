# FUTURE_DS_01 — Business Sales Data Analysis
### FutureInterns Internship · Task 1 of 3

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) 
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Chart.js](https://img.shields.io/badge/Chart.js-Dashboard-ff6384?logo=chartdotjs)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Task Overview

Analyze business sales data to identify:
- **Revenue trends** over time
- **Top-selling products** by revenue and volume
- **High-value regions** and country-level performance
- **Actionable recommendations** for business growth

---

## 📁 Project Structure

```
FUTURE_DS_01/
│
├── dashboard.html        # 🎨 Interactive client-ready dashboard (open in browser)
├── analysis.py           # 🐍 Python analysis & KPI computation script
├── README.md             # 📄 This file
│
└── (generated on run)
    ├── monthly_revenue.csv
    ├── top_products.csv
    ├── top_countries.csv
    └── quarterly_revenue.csv
```

---

## 📊 Dataset

| Field | Detail |
|---|---|
| **Source** | UCI Online Retail Dataset |
| **File** | `online_retail.csv` |
| **Rows** | 541,909 transactions |
| **Period** | December 2010 – December 2011 |
| **Countries** | 38 |
| **Columns** | InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country |

---

## 🔢 Key KPIs

| Metric | Value |
|---|---|
| Total Revenue | **£10.67 Million** |
| Total Orders | **22,190** |
| Unique Customers | **4,338** |
| Unique Products | **4,026** |
| Average Order Value | **£534** |
| Countries Served | **38** |
| Cancellation Rate | **1.7%** (healthy) |

---

## 📈 Key Insights

### 1. 📈 Revenue Trend — Strong Growth Trajectory
- Revenue grew from £823K in Q4 2010 to **£3.3M in Q4 2011** — a 4x increase.
- November 2011 was the **single highest revenue month (£1.51M)**.
- Clear seasonal uplift pattern every Q4 (holiday/gifting season).

### 2. 🏆 Star Products
| Product | Revenue |
|---|---|
| Regency Cakestand 3 Tier | £174,485 |
| Paper Craft, Little Birdie | £168,470 |
| White Hanging Heart T-Light Holder | £106,293 |
| Party Bunting | £99,504 |

### 3. 🌍 Regional Performance
- **United Kingdom** dominates with **85% of total revenue (£9.03M)**.
- Netherlands (£285K), EIRE (£283K), and Germany (£229K) are the next largest markets.
- Significant international growth opportunity in Germany and France.

### 4. 💡 Recommendations
1. **Seasonal campaigns**: Pre-load inventory and launch campaigns by September to capture Q4 holiday surge.
2. **International expansion**: Run targeted paid campaigns in Germany & France — both show high order frequency.
3. **Bundling strategy**: Pair high-volume low-margin products with premium items to raise average order value.
4. **AOV nudge**: Introduce free-shipping threshold above £600 to push the current £534 AOV upward.
5. **Stock protection**: Maintain buffer inventory for top 10 revenue products — stockouts on these directly hurt revenue.

---

## 🛠️ How to Run

### Prerequisites
```bash
pip install pandas numpy
```

### Run Analysis
```bash
# Place online_retail.csv in the same folder, then:
python analysis.py
```

### View Dashboard
Simply open `dashboard.html` in any modern web browser. No server needed.

---

## 🖼️ Dashboard Preview

The interactive dashboard includes:
- ✅ 6 KPI summary cards
- ✅ Monthly revenue trend line chart
- ✅ Quarterly revenue + growth rate combo chart
- ✅ Top 10 products ranked table with mini bar charts
- ✅ Revenue by country horizontal bar chart
- ✅ Top products by units sold
- ✅ Market share doughnut chart
- ✅ Revenue vs Orders dual-axis chart
- ✅ 4 insight cards with actionable recommendations

---

## 🧹 Data Cleaning Steps

1. Removed **cancelled orders** (InvoiceNo starting with 'C') — 9,288 rows
2. Removed rows with **negative or zero Quantity** 
3. Removed rows with **zero or negative UnitPrice**
4. Dropped rows with **missing Description**
5. Parsed `InvoiceDate` to datetime format
6. Computed `Revenue = Quantity × UnitPrice`
7. Extracted `Month`, `Quarter`, `Year` features

---

## 📚 Tools Used

| Tool | Purpose |
|---|---|
| Python + Pandas | Data cleaning, KPI analysis |
| Chart.js (CDN) | Interactive dashboard charts |
| HTML + CSS | Client-ready dashboard UI |

---

## 👤 Author

**[Your Name]**  
FutureInterns Data Analytics Internship  
Task 1 of 3 · FUTURE_DS_01

---

*For Task 2, refer to FUTURE_DS_02 repository.*
