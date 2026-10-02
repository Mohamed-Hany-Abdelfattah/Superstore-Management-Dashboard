# 📊 Superstore Sales Analysis Dashboard

Interactive **Microsoft Excel** management dashboard analyzing **4 years** of retail sales (**2016–2019**) for a US superstore chain — **9,993 line items · 5,009 orders · 793 customers · $2.29M in sales**, driven by a live **Filter Panel** and 5 native charts.

> **Tool:** Microsoft Excel (PivotTables, Slicers, Excel Tables, Conditional Formatting, Charts) | **Data Source:** Kaggle — *Superstore Sales Dataset*

---

## 📌 Overview

A self-contained **Data Cleaning → Analysis → Dashboard** pipeline inside a single `.xlsx` file:

```
Raw Data  →  Clean Data  →  Analysis  →  SUPERSTORE DASHBOARD
 (source)      (prepared)     (pivots)       (live view)
```

The dashboard is fully interactive — slicer selections on the **Filter Panel** propagate through every KPI card, chart, and pivot table with no manual recalculation.

---

## 🧾 Headline Figures

| Metric | Value |
|--------|-------|
| Total Sales | **$2,296,919.49** |
| Total Profit | **$286,409.08** |
| Profit Margin | **12.47%** |
| Average Order Value | $57.18 |
| Unique Orders | 5,009 |
| Unique Customers | 793 |
| Period | 2016-01-03 → 2019-12-30 |
| Avg. Discount | 15.6% |

---

## 📜 Performance by Region

| Region | Sales | Profit | Margin % |
|--------|------:|-------:|---------:|
| West | $725,457.82 | $108,418.45 | **14.94%** |
| East | $678,499.87 | $91,534.84 | 13.49% |
| Central | $501,239.89 | $39,706.36 | 7.92% |
| South | $391,721.91 | $46,749.43 | 11.93% |

## 📜 Performance by Category

| Category | Sales | Profit | Margin % |
|----------|------:|-------:|---------:|
| Technology | $836,154.03 | $145,454.95 | 17.40% |
| Furniture | $741,718.42 | $18,463.33 | **2.49%** |
| Office Supplies | $719,047.03 | $122,490.80 | 17.04% |

## 📜 Performance by Segment

| Segment | Sales | Profit | Margin % | Line Items |
|---------|------:|-------:|---------:|-----------:|
| Consumer | $1,161,401.34 | $134,119.21 | 11.55% | 5,191 |
| Corporate | $706,146.37 | $91,979.13 | 13.03% | 3,020 |
| Home Office | $429,371.78 | $60,310.74 | 14.05% | 1,782 |

---

## 📄 Workbook Contents (5 Sheets)

### Sheet 1 — `Raw Data`
- **9,994 rows × 21 columns** of untouched transactional records, formatted as a native **Excel Table** (`tblRawData`).
- Covers order identity, dates, ship mode, customer geography, product hierarchy, and the `Sales` / `Quantity` / `Discount` / `Profit` measures.

### Sheet 2 — `Clean Data`
- **9,993 rows** — a single duplicate row removed, with **5 engineered columns** appended:

| Derived Column | Purpose |
|----------------|---------|
| `Profit Margin` | Profit ÷ Sales |
| `Sales Category` | High / Medium / Low sales banding |
| `Profit Status` | Profit / Loss flag |
| `Year` | Order year (2016–2019) |
| `Year-Month` | Monthly bucket for trend analysis |

- Stored as a native Excel Table (`tblCleanData`) so downstream pivots auto-expand.

### Sheet 3 — `SUPERSTORE DASHBOARD`
The executive view. Contains:

- **5 KPI cards** — Total Sales, Total Profit, Profit Margin, Top Region, Total Orders.
- **5 Charts** — visuals wired to the pivot-driven analysis sheet.
- **Filter Panel with Slicers** — drill into Region, Category, Segment, and Ship Mode.
- **4 highlight cards** — Top Region, Top Product, Best Category, Best Sales Month.

### Sheet 4 — `Analysis`
Seven pivot analyses backing the dashboard visuals:
1. Sales by Region (with margin %)
2. Profit by Category
3. Sales by Segment
4. Sales & Profit by Ship Mode (cross-tabbed by category)
5. Sales & Profit by Sub-Category
6. Top 10 Products by Sales (with units sold & margin)
7. Monthly Sales & Profit Trend (2016–2019)

### Sheet 5 — `Dashboard Data`
PivotTable caches and helper ranges that feed the dashboard charts.

---

## 🧠 Key Insights

- **Furniture is the profit sink.** It generates the **2nd-highest sales** ($741.7K) but only a **2.49% margin** ($18.5K) — roughly one-eighth of Technology's margin on comparable revenue.
- **Tables lose money.** The `Tables` sub-category is the single worst performer at **−$17,725.48 profit (−8.56% margin)**, alongside loss-making `Bookcases` and `Supplies`.
- **Discounting is the root cause.** The average discount is **15.6%**, and **52% of all line items** carry a discount — heavily discounted lines are where margins collapse.
- **Copiers and Paper are the profit engines.** `Copiers` (**37.20%**) and `Paper` (**43.39%**) post the healthiest margins despite mid-tier sales.
- **West region leads on both sales and margin** (14.94%), while **Central** is margin-poor at 7.92% despite $501K in revenue.
- **Smaller segments are more profitable.** Home Office (14.05%) outperforms Consumer (11.55%) on margin.

---

## 🔁 Getting Started

1. **Download:** [`Superstore 2019.xlsx`](Superstore%202019.xlsx)
2. Open in **Microsoft Excel 2016 or later** (slicers require Excel 2013+).
3. Open the **`SUPERSTORE DASHBOARD`** sheet — use the **Filter Panel** to slice the data by region, category, segment, or ship mode.
4. All charts and KPIs update live.

> ⚠️ Enable **macros-free** viewing — the workbook contains **no VBA**. It relies only on native Excel features.

---

## 📦 Data Source

This project uses the widely available **[Superstore Sales Dataset](https://www.kaggle.com/datasets/vediarya/superstore-sales-dataset)** published on Kaggle, a sample retail transaction dataset. Credit for the underlying dataset belongs to its original author; the cleaning, derived columns, pivot analysis, and dashboard design in this repository are original work.

---

## 📦 File Structure

```text
superstore-sales-analysis/
├── Superstore 2019.xlsx   # Main workbook (5 sheets)
└── README.md              # Project documentation
```

---

## 🔗 Connect

- **Author:** Mohamed Hany
- **LinkedIn:** [Mohamed Hany Abdelfattah](https://www.linkedin.com/in/mohamed-hany-abdelfattah/)
- **GitHub:** [Mohamed-Hany-Abdelfattah](https://github.com/Mohamed-Hany-Abdelfattah/)
