**Author:** Zainab R. Ogunjobi
**Tools:** Microsoft Excel · Power BI
**Dataset:** SuperStore US Sales Dataset
**Status:** ✅ Completed

---

## 📌 Project Overview

This project analyses **2 years of retail sales data** from a fictional US-based SuperStore chain, covering 3,003 orders across 4 regions, 3 product categories, and 3 customer segments. The goal was to identify revenue trends, profitability by category, regional performance, and customer behaviour — delivering actionable insights to support strategic business decisions.

The analysis was completed using **Excel for data cleaning and exploration**, and **Power BI for interactive dashboard visualisation**.

---

## ❓ Key Business Questions

1. How did total sales and profit grow from 2019 to 2020?
2. Which product categories and sub-categories are most profitable?
3. Which regions and states drive the most revenue?
4. Which customer segments contribute most to sales?
5. How do shipping modes and payment methods affect business operations?
6. Which months are the strongest and weakest for sales performance?

---

## 📁 Repository Structure

```
superstore-sales-dashboard/
│
├── data/
│   └── SuperStore_Sales_Dataset.csv         ← Raw sales dataset
│
├── analysis/
│   └── superstore_analysis.xlsx             ← Pivot tables & calculated fields
│
├── dashboard/
│   └── superstore_dashboard.pbix            ← Power BI interactive dashboard
│   └── dashboard_preview.png                ← Screenshot of final dashboard
│
├── visuals/
│   ├── sales_by_category.png                ← Bar chart — category performance
│   ├── sales_by_region.png                  ← Map/bar — regional breakdown
│   ├── monthly_trend.png                    ← Line chart — monthly sales trend
│   ├── profit_margin_by_category.png        ← Margin comparison chart
│   └── segment_breakdown.png                ← Customer segment analysis
│
└── README.md
```

---

## 🗃️ Dataset Overview

| Detail | Info |
|--------|------|
| Source | SuperStore US Retail Dataset (Practice Dataset) |
| Period | January 2019 — December 2020 |
| Total Orders | 3,003 |
| Total Records | 5,901 |
| Total Customers | 773 |
| Total Units Sold | 22,317 |

**Key Columns:**

| Column | Description |
|--------|-------------|
| Order ID | Unique order identifier |
| Order Date / Ship Date | Order and shipping dates |
| Ship Mode | Standard, Second Class, First Class, Same Day |
| Customer ID / Name | Customer details |
| Segment | Consumer, Corporate, Home Office |
| Region / State / City | Geographic location |
| Category / Sub-Category | Product classification |
| Sales | Revenue per order line |
| Quantity | Units sold |
| Profit | Profit per order line |
| Returns | Returned order value |
| Payment Mode | COD, Online, Cards |

---

## 🧹 Data Preparation Steps

Performed in **Excel** before analysis:

- ✅ Removed encoding artifacts from column headers (BOM characters from CSV export)
- ✅ Converted `Order Date` and `Ship Date` to proper date format (DD-MM-YYYY)
- ✅ Extracted `Month`, `Year`, and `Quarter` columns for time-series analysis
- ✅ Dropped irrelevant index columns (`ind1`, `ind2`)
- ✅ Verified zero duplicate Order IDs within same product lines
- ✅ Checked and confirmed minimal null values across key fields
- ✅ Calculated `Profit Margin %` = Profit / Sales × 100
- ✅ Calculated `Days to Ship` = Ship Date − Order Date for delivery analysis

---

## 📊 Key Findings & Insights

### 💰 Overall Business Performance

| KPI | Value |
|-----|-------|
| Total Sales (2 Years) | **$1,565,804** |
| Total Profit | **$175,262** |
| Overall Profit Margin | **11.2%** |
| Total Orders | **3,003** |
| Total Units Sold | **22,317** |
| Unique Customers | **773** |

> 🔍 **Insight:** At 11.2%, the SuperStore's profit margin is relatively thin for a retail operation. This signals a need to review pricing strategy, reduce discounting, or shift product mix toward higher-margin categories.

---

### 📈 Revenue Growth by Year

| Year | Total Sales | Growth |
|------|-------------|--------|
| 2019 | $564,680 | Baseline |
| 2020 | $1,001,125 | **+77.3% YoY** |

> 🔍 **Insight:** Revenue grew by 77% in 2020 — a remarkable result that likely reflects business expansion, new customer acquisition, and increased order volumes. This growth trajectory is a strong signal for continued investment.

---

### 📦 Sales & Profit by Category

| Category | Total Sales | Total Profit | Margin |
|----------|-------------|--------------|--------|
| Office Supplies | $643,708 (41%) | $74,797 | 11.6% |
| Technology | $470,588 (30%) | $90,458 | **19.2%** |
| Furniture | $451,509 (29%) | $10,007 | **2.2%** |

> 🔍 **Insight:** **Technology is the profit engine** — despite being 2nd in sales volume, it delivers the highest profit margin at 19.2%. Furniture is a major concern — nearly $452K in sales generates just $10K profit (2.2% margin), suggesting high costs, heavy discounting, or returns dragging profitability down significantly.

---

### 🏆 Top 5 Sub-Categories by Sales

| Rank | Sub-Category | Sales |
|------|-------------|-------|
| 1 | Phones | $196,564 |
| 2 | Chairs | $181,946 |
| 3 | Binders | $174,978 |
| 4 | Storage | $150,341 |
| 5 | Accessories | $122,301 |

> 🔍 **Insight:** Phones and Accessories (both Technology) together generate strong revenue with healthy margins. Chairs (Furniture) rank 2nd in sales but likely contribute minimally to profit given the category's 2.2% margin.

---

### 🗺️ Sales by Region

| Region | Total Sales | Share |
|--------|-------------|-------|
| West | $522,441 | 33% |
| East | $450,235 | 29% |
| Central | $341,008 | 22% |
| South | $252,121 | 16% |

> 🔍 **Insight:** The **West and East regions dominate**, accounting for 62% of total sales. The South is significantly underperforming — targeted marketing and regional promotions could unlock meaningful revenue growth in this territory.

---

### 🌎 Top 5 States by Revenue

| State | Total Sales |
|-------|-------------|
| California | $335,190 |
| New York | $186,748 |
| Texas | $116,262 |
| Washington | $92,975 |
| Pennsylvania | $82,355 |

> 🔍 **Insight:** California alone accounts for **21% of total revenue** — a significant geographic concentration. Texas, despite being the 2nd largest US state by population, ranks 3rd, suggesting untapped market potential.

---

### 👥 Sales by Customer Segment

| Segment | Total Sales | Share |
|---------|-------------|-------|
| Consumer | $753,002 | 48% |
| Corporate | $509,743 | 33% |
| Home Office | $303,059 | 19% |

> 🔍 **Insight:** **Consumer segment leads but Corporate offers higher growth potential** — corporate clients typically have larger order sizes and longer-term relationships. A dedicated B2B sales strategy could significantly grow the Corporate segment share.

---

### 🚚 Sales by Shipping Mode

| Ship Mode | Sales | Share |
|-----------|-------|-------|
| Standard Class | $912,401 | 58% |
| Second Class | $314,508 | 20% |
| First Class | $242,937 | 16% |
| Same Day | $95,959 | 6% |

> 🔍 **Insight:** Standard Class dominates at 58% — reflecting cost-conscious customer behaviour. The low uptake of Same Day (6%) and First Class (16%) shipping suggests either price sensitivity or lack of awareness of premium options.

---

### 💳 Sales by Payment Mode

| Payment Mode | Sales | Share |
|-------------|-------|-------|
| COD (Cash on Delivery) | $667,418 | 43% |
| Online | $553,993 | 35% |
| Cards | $344,393 | 22% |

> 🔍 **Insight:** COD at 43% is the dominant payment method — which creates cash flow challenges and higher operational costs compared to digital payments. Incentivising online and card payments through discounts or loyalty rewards could meaningfully improve working capital management.

---

### 📅 Monthly Sales Trend

| Peak Months | Sales | Slow Months | Sales |
|-------------|-------|-------------|-------|
| December | $244,585 | January | $73,380 |
| November | $210,373 | February | $72,047 |
| September | $193,214 | April | $89,558 |

> 🔍 **Insight:** **Q4 (Oct–Dec) is the clear peak season**, driven by holiday and year-end purchasing. September also spikes — likely driven by back-to-school and corporate budget cycles. January and February are the weakest months — ideal for promotional campaigns or clearance sales.

---

## 💡 Business Recommendations

1. **Prioritise Technology sales** — at 19.2% margin it is the most profitable category. Expanding the product range, upselling accessories, and bundling products could maximise revenue per order.

2. **Address Furniture profitability** — 2.2% margin on $451K revenue is unsustainable. Review discounting policies, supplier costs, and return rates specifically for Furniture items.

3. **Grow the Corporate segment** — dedicated account managers, volume discounts, and B2B outreach targeting corporate clients could unlock a higher-value revenue stream.

4. **Reduce COD dependency** — introduce incentives for Online and Card payments to improve cash flow and reduce delivery risk from unaccepted COD orders.

5. **Invest in Southern states** — at 16% of sales, the South is significantly underperforming. Targeted campaigns in Florida, Georgia, and North Carolina could unlock new revenue.

6. **Capitalise on Q4 demand** — stock, marketing, and logistics should be scaled up aggressively from August to prepare for the September–December peak.

---

## 🛠️ How to Explore This Project

**Data File:**
1. Open `SuperStore_Sales_Dataset.csv` in Excel or Google Sheets
2. Apply filters by Category, Region, or Segment to explore the data

**Power BI Dashboard:**
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Open `superstore_dashboard.pbix`
3. Use slicers to filter by Year, Region, Category, Segment, and Payment Mode

---

## 🚀 Skills Demonstrated

- ✅ CSV data cleaning and preparation
- ✅ Date formatting and time-series extraction
- ✅ Multi-dimensional pivot analysis (category, region, segment, channel)
- ✅ Profitability and margin analysis
- ✅ Customer segmentation analysis
- ✅ Payment and logistics behaviour analysis
- ✅ Power BI interactive dashboard design
- ✅ Business insight generation and strategic recommendations

---

## 👩‍💻 About the Author

**Zainab R. Ogunjobi** is an Economics graduate and data analyst based in Lagos, Nigeria, with hands-on experience in financial reporting, data management, and business performance analysis.

🌐 [Portfolio](https://zainab-ogunjobi-va.netlify.app) · 💼 [LinkedIn](https://linkedin.com/in/ogunjobi-zainab) · 📧 [Email](mailto:Zainabogunjobir@gmail.com)

---

*Part of my Data Analytics Portfolio — feel free to fork or reach out with feedback!*
