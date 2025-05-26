# AtliQ-s-Data-Analysis

This project aims to provide actionable insights into AtliQ’s sales performance using Microsoft Excel’s advanced analytics capabilities. By transforming raw data using Power Query, building relationships via Power Pivot, and crafting insightful reports with PivotTables and DAX measures, the objective is to evaluate customer contributions, market target achievements, and profitability across fiscal years and quarters. The analysis enhances data-driven decision-making with clear visuals, trends, and performance indicators, ultimately helping stakeholders optimize strategies in customer management, regional targeting, and product division performance.


🛠️ ETL Process & Data Modeling
🔹 Extract
  ~ Imported datasets from multiple sheets including sales, product, customer, market, and date dimensions.
  
🔹 Transform
  ~ Cleaned raw data using Power Query (removed nulls, blanks, merged columns).
  ~ Added key calculated columns:
  ~ Fiscal Year
  ~ COGS (Manufacturing Cost + Freight + Other Expenses)
  ~ Gross Margin and Gross Margin %
  ~ Quarter (based on fiscal calendar)

🔹 Load
  ~ Loaded refined data into Power Pivot.
  ~ Defined relationships between:
  ~ fact_sales_monthly and dim_customer, dim_product, dim_market, dim_date.
  

📊 Analysis 1: Customer Performance Report
🔹 Purpose
  ~ Evaluate customer-wise performance and sales growth over 2019, 2020, and 2021.

🔹 Key Metrics
  ~ Net Sales (yearly): Pulled from fact_sales_monthly
  ~ Growth from 2020 to 2021:
    ~ Formula:
      (NetSales2021−NetSales2020)/NetSales2020×100

🔹 Insights
  ~ Identified best-performing customers (e.g., Amazon, Croma, BestBuy).
  ~ Spotted key growth opportunities and stagnating accounts.
  ~ Provided actionable sales trends for account managers.

🔹 Visuals & Formatting
  ~ Sales shown in millions for better readability.
  ~ Conditional formatting used to highlight:
  ~ Top 3 customers
  ~ Customers with declining sales

📈 Analysis 2: Market Performance vs Target (2021)
🔹 Purpose
  ~ Compare actual 2021 sales performance against predefined targets by country.

🔹 Key Metrics
  ~ Net Sales (actual) vs Target Sales (goal)
  ~ Performance Gap: Net Sales - Target
  ~ Achievement %: (Net Sales / Target) * 100

🔹 Findings
  ~ Overachieving countries: India, USA, Canada
  ~ Underperforming countries: France, Germany
  ~ Suggested resource reallocation or campaign improvements in lagging regions.

🔹 Visual Enhancements
  ~ Bar charts to contrast targets vs actuals.
  ~ Traffic light color coding (Green = Achieved, Red = Underperformed).

💰 Analysis 3: P&L by Fiscal Year
🔹 Purpose
  ~ Analyze annual profitability and financial health for 2019, 2020, and 2021.

🔹 Key Metrics
  ~ Net Sales
  ~ COGS (custom-calculated)
  ~ Gross Margin = Net Sales - COGS
  ~ Gross Margin % = Gross Margin / Net Sales * 100

🔹 Growth Evaluation (2020 → 2021)
  ~ Added columns for:
  ~ Increment:
      Value 2021 - Value 2020
  ~ Growth %:
      (Value 2021 - Value 2020) / Value 2020 * 100
  ~ Applied to all four metrics: Net Sales, COGS, Gross Margin, and Gross Margin %

🔹 Strategic Insights
  ~ Revenue and margin consistently improved year-over-year.
  ~ Cost control effective despite operational scale-up.

🔹 Report View
  ~ Year-wise PivotTables with increment and growth columns for side-by-side comparison.
  ~ % Growth color-coded to show financial performance trends.

📆 Analysis 4: Quarterly P&L Report
🔹 Purpose
  ~ Break down the P&L data into quarters and months for detailed analysis.
  
🔹 Fiscal Quarter Mapping
  ~ Q1: Sep–Nov
  ~ Q2: Dec–Feb
  ~ Q3: Mar–May
  ~ Q4: Jun–Aug

🔹 Key Metrics (Monthly & Quarterly)
  ~ Net Sales
  ~ COGS
  ~ Gross Margin
 ~ Gross Margin %

🔹 Increment & Growth (2020 → 2021)
  ~ Just like the annual P&L, this report includes:
  ~ Increment columns for Net Sales, COGS, Gross Margin, GM %.
  ~ Growth % columns to show year-over-year change for each quarter.

🌟 Final Highlights & Reporting Features
✅ Design & Usability
  ~ Sales values converted to millions (e.g., ₹2.3M) for clean visuals.
  ~ Clear report headers and section labels used across sheets.

✅ Performance Indicators
  ~ Conditional formatting to emphasize:
  ~ High/low performers
  ~ Sales dips and growth spikes
  ~ Filters applied to allow region-wise, market-wise, and division-wise slicing.

✅ Stakeholder Value
  ~ Easy interpretation through PivotTables.
  ~ Actionable insights provided in a clear, visual-first layout.
  ~ Custom DAX measures provide dynamic, real-time updates for future data integration.







📊 AtliQ Finance & Sales Analysis – Key Takeaways (2019–2021)
1️⃣ Exponential Revenue Growth
Net Sales Surge:
From $87.48M (2019) to $598.88M (2021) → 585% growth in 3 years.

Year-on-Year (YoY) Growth (2020 → 2021):
+204%, from $196.69M to $598.88M.

🏆 Top Performing Customers
Amazon: $12.17M → $82.09M

Flipkart: $2.94M → $19.29M

AtliQ Exclusive: $9.58M → $61.12M (538% growth)

2️⃣ Gross Margin Challenges
Declining GM%:
From 41.4% (2019) → 36.4% (2021), signaling increased costs or pricing pressure.

📉 Key GM% Decliners
Amazon: 41.5% → 35.3%

Flipkart: 34.8% → 30.2%

📈 Best GM% Performers (2021)
Electricalsquipo Stores: 47.2%

Chip 7: 40.7%

3️⃣ Customer-Centric Insights
🚀 High-Growth Customers
Nova: 13.2K → 351.2K (26.6x growth)

Integration Stores: 162.8K → 1.44M (8.9x growth)

⚠️ Underperforming Customers
Notebillig: GM% at 18.3%

Viveks: GM% dropped to 26.5%

4️⃣ Market Expansion & Performance
🌍 Top Markets in 2021
India: $161.26M (missed target by $9.55M)

USA: $87.78M (missed target by $10.24M)

South Korea: $48.97M (missed target by $4.36M)

🌱 Emerging Markets
Bangladesh: $0.48M → $6.95M

Indonesia: $6.13M → $18.41M (3x growth)

5️⃣ Quarterly Trends (2021)
Steady Growth: Quarterly revenue ranged from $44.8M to $78.1M.

Peak in Q4 (Dec): $78.06M, likely due to holiday seasonality.

6️⃣ Target vs. Actual (2021)
Total Shortfall: Missed 2021 global sales target by $54.94M (8.4%)

🚨 Largest Gaps
USA: -$10.24M

Canada: -$5.07M

✅ Near Target
China: -$2.07M

France: -$2.19M (7.8% gap)

🎯 Strategic Impact
✅ Scalability Success: Effective market penetration, especially in India and USA.

⚠️ Profitability Pressure: Falling GM% → need for cost control or price strategy update.

🚀 High-Potential Customers: Focus on fast-growing accounts like Nova and Integration Stores.

🌍 Market Prioritization: Improve performance in Canada and Germany; double down on South Korea and Indonesia.

🧭 Target Realignment: Adjust 2022 goals based on 2021 shortfalls and growth opportunities.

📌 Conclusion:
AtliQ's rapid growth is remarkable, but sustaining profitability and meeting targets will require sharper focus on cost efficiency, customer prioritization, and market-specific strategies.
