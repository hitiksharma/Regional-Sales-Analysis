# Regional Sales Analysis: EDA, Feature Engineering & Power BI Dashboarding
 
An end-to-end sales analytics project analyzing **$1.24 billion** in revenue across **64,104 orders**, **175 customers**, and **30 products** over 5 years (2014–2018). Combines Python-based EDA with Power BI interactive dashboarding to uncover revenue drivers, profit patterns, and growth opportunities.
 
**Author:** Hitik Sharma | M.Sc. Computer Science, University of Passau  
**GitHub:** [github.com/hitiksharma](https://github.com/hitiksharma)  
**LinkedIn:** [linkedin.com/in/hitik-sharma-29966a18b](https://www.linkedin.com/in/hitik-sharma-29966a18b/)
 
---
 
## Project Overview
 
**Problem Statement:** Sales teams often lack a clear, data-driven understanding of regional performance, making it difficult to identify growth opportunities and optimize resources.
 
**Goal:** Leverage 5 years of historical data to pinpoint growth levers and optimize strategy across products, channels, regions, and customers.
 
**Approach:**
1. Business objective definition
2. Data collection and consolidation (6 relational tables from Excel)
3. Data profiling, cleaning, and merging using ER diagram analysis
4. Feature engineering (profit, profit margin, cost calculations)
5. Exploratory Data Analysis (EDA) with 15+ visualizations
6. Power BI interactive dashboard for stakeholder reporting
---
 
## Key Results
 
| Metric | Value |
|--------|-------|
| Total Revenue | **$1.24 Billion** |
| Total Profit | **$462 Million** |
| Average Profit Margin | **37.4%** |
| Orders Analyzed | **64,104** |
| Customers | **175** |
| Products | **30** |
| Time Period | **2014 – 2018** |
 
---
 
## Key Insights
 
### Revenue by Channel
- **Wholesale:** $668M (54.1%) — highest volume
- **Distributor:** $387M (31.3%)
- **Export:** $181M (14.6%) — highest profit margin
### Top Products
- **Product 26:** $112M (highest revenue)
- **Product 25:** $106M
- Sharp drop after top 2 — Product 13 at $75M
### Top States
- **California:** $229M (dominant market)
- **Illinois:** $111M
- **Florida:** $90M
- **Texas:** $84M
### Seasonal Patterns
- **May** is the highest-grossing month overall
- Downward spikes at start of each year (January dips)
- Revenue cycles between $23–26M monthly
### Customer Insights
- Aibox is the top customer by revenue
- Some mid-revenue customers (6–8M) show highest profit margins
- Extreme concentration: top 10 customers drive significant portion of total revenue
### Correlations
- Unit price and revenue: **strongly correlated**
- Profit and revenue: **highly correlated**
- Order quantity shows weaker correlation with revenue
---
 
## Data Architecture
 
The project integrates 6 relational tables through a documented Entity Relationship Diagram:
 
| Table | Records | Key Fields |
|-------|---------|------------|
| Sales Orders | 64,104 | Order number, date, customer, product, revenue |
| Customers | 175 | Customer index, name |
| Products | 30 | Product index, name |
| Regions | 994 | Location, state, county, population, income |
| State Regions | 49 | State code, state name, region |
| 2017 Budgets | 30 | Product name, budget amount |
 
All tables were merged using primary/foreign key relationships identified through ER diagram analysis.
 
---
 
## Technical Implementation
 
### Python EDA (Jupyter Notebook)
- **Data Merging:** 5 left joins connecting Sales Orders → Customers → Products → Regions → State Regions → Budgets
- **Data Cleaning:** Redundant column removal, header correction, lowercase standardization, 2018 partial data handling
- **Feature Engineering:** `total_cost`, `profit`, `profit_margin_pct`, month extraction
- **Visualizations:** Monthly revenue trends, top/bottom 10 products, channel distribution (pie chart), AOV distribution, unit price boxplots, state revenue rankings, customer segmentation scatter plot, correlation heatmap
### Power BI Dashboard
- Interactive dashboard with filters for year, region, channel, and product
- KPI cards for total revenue, profit, and margin
- Regional performance maps
- Product and customer drill-down views
---
 
## Repository Structure
 
```
Regional-Sales-Analysis/
├── README.md
├── Sales_Analysis.ipynb          # Complete Python EDA notebook
├── Regional_Sales_Dataset.xlsx   # Source data (6 sheets)
├── Final_Regional_sales.csv      # Cleaned, merged dataset
├── SALES_REPORT.pbix             # Power BI dashboard file
├── ER_diagram.png                # Entity Relationship Diagram
```
 
---
 
## How to Run
 
```bash
# Clone the repository
git clone https://github.com/hitiksharma/Regional-Sales-Analysis.git
cd Regional-Sales-Analysis
 
# Install Python dependencies
pip install pandas numpy matplotlib seaborn openpyxl
 
# Open the notebook
jupyter notebook Sales_Analysis.ipynb
 
# For Power BI: Open SALES_REPORT.pbix in Power BI Desktop
```
 
---
 
## Tools & Technologies
 
- **Python:** pandas, NumPy, matplotlib, seaborn
- **Power BI:** Interactive dashboards, DAX measures, data modeling
- **Data Engineering:** Multi-table joins, ER diagram design, feature engineering
- **Analysis:** EDA, statistical analysis, customer segmentation, trend analysis
---
 
## License
This project is for educational and portfolio purposes.
