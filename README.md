[Financials.csv](https://github.com/user-attachments/files/33863295/Financials.csv)# Sales-Performance-Analysis-
End-to-end Business Intelligence project analyzing 2-year multinational sales data to uncover $128M revenue drivers, product profitability, and discount strategy failures.

### 🔴 Live Dashboard Preview
<img width="988" height="555" alt="recent plan work" src="https://github.com/user-attachments/assets/8324bb5c-086c-4647-b35e-02ff76a97345" />
<img width="988" height="555" alt="page 2 recent" src="https://github.com/user-attachments/assets/225567bb-1273-48bf-b904-fb3ef1610ea2" />
<img width="986" height="555" alt="page 3 " src="https://github.com/user-attachments/assets/22fdcc09-695d-4d13-a512-0ec8c2c24328" />


### 📌 Project Overview
This project transforms raw financial data into 3 interactive dashboards for C-level decision making. The dataset contains sales transactions across 5 countries, 5 market segments, 6 products, and 2 years (2013-2014).

**Business Questions Answered:**
- Which market segment and country drives maximum profit?
- Which product is the cash cow vs underperformer?
- Is our discount strategy helping or killing margin?
- What caused 114% sales growth in December?

### 📈 Key Insights

**Executive KPIs:**
- **Total Sales:** $128M | **Units Sold:** 1.02M | **Total Profit:** $26M | **Avg Discount:** 7% | **Profit Margin:** 20%

**1. Market Performance:**
- Government (44% / $56M) + Small Business (36% / $46M) = 80% of total revenue. Channel Partners is only 2% - major opportunity.
- Canada is most profitable market ($5.57M), despite 8% discount.

**2. Product Profitability:**
- **Paseo is the MVP:** $7.39M profit. Manufacturing Cost: $10.00 vs Sale Price: $108.18 (980% markup)
- VTT & Amarilla have high manufacturing costs ($250 & $260) - need supply chain optimization.
- COGS vs Profit: Paseo consumes $28M COGS but returns highest profit - best ROI.

**3. Discount Strategy - The Critical Finding:**
- **Paradox Found:** High Discount = 398K units sold (highest) but only 34% margin.
- **No Discount = 37% margin** (Highest). Low Discount = 30% (Lowest).
- 66% of revenue depends on High + Medium discounts. Business is over-discounting.

### 🛠️ Tools & Techniques

| Tool | Use |
| :--- | :--- |
| **Power BI Desktop** | Dashboarding & Visualizations |
| **Power Query** | Data Cleaning, Parsing `mm/yy` to Date/Year/Month |
| **DAX** | KPI Measures & Calculations |
| **Excel** | Raw Data Source |

**Key DAX Measures:**
```DAX
Total Sales = SUM(Financials[Sales])
Total Profit = SUM(Financials[Profit])
Profit Margin % =[Financials.csv](https://github.com/user-attachments/files/33863639/Financials.csv)
 DIVIDE([Total Profit], [Total Sales])
Sales Growth % = DIVIDE([Sales CY] - [Sales PY], [Sales PY])
Avg Manufacturing Price = AVERAGE(Financials[Manufacturing Price])
Segment,Country, Product , Discount Band , Units Sold , Manufacturing Price , Sale Price , Gross Sales , Discounts ,  Sales , COGS , Profit ,Date,Month Number, Month Name ,Year
