# Superstore Sales & Profit Analysis Dashboard
Interactive Excel Dashboard for Superstore Sales & Profit Analysis (2015–2018), This project features an interactive Excel dashboard built to analyze comprehensive retail performance using the Sample Superstore dataset (2015–2018). The primary goal is to transform raw sales data into actionable, visual insights regarding product profitability, customer segment behaviors, and regional trends.

<img width="1697" height="761" alt="image" src="https://github.com/user-attachments/assets/9e2c169c-fc34-4294-a7ac-2a9958c76198" />

## Business Questions Framework

| Dimension | Key Business Questions |
| :--- | :--- |
| **Sales** | 1. What are the monthly and yearly sales and profit trends (2015–2018)?<br>2. Which quarters or months generate the highest profit? |
| **Product** | 1. Which sub-categories are the most profitable, and which ones incur losses?<br>2. Which products drive the highest overall sales revenue? |
| **Customer** | 1. Which customer segment (Consumer, Corporate, Home Office) is the most profitable? |
| **Location** | 1. Which top 10 states contribute the highest total profit? |

## Data Cleaning & Preparation Process

Before constructing the pivot tables and visualization modules, the raw dataset underwent a structured data cleaning and transformation workflow using **Power Query** in Excel:

1. **Duplicate Check & Removal**: Verified unique order records and removed duplicate rows to avoid double-counting sales volume.
2. **Missing Value Handling**: Identified blank entries in critical fields (such as Postal Code and Sub-Category) and replaced/imputed missing values or dropped unresolvable records.
3. **Data Type Validation**: Corrected field data types (e.g., set `Order Date` & `Ship Date` to `Date`, `Sales` & `Profit` to `Currency / Decimal Number`, and `Quantity` to `Whole Number`).
4. **Column Standardization (CamelCase / Naming Convention)**: Standardized all column headers into clear, consistent formats (e.g., `OrderDate`, `ShipMode`, `SubCategory`, `ProfitMargin`) to streamline DAX and Pivot Table operations.
5. **Feature Engineering & Calculated Fields**:
   - Extracted `Year`, `Month`, `Quarter`, and `Day of Week` from `Order Date` for timeline aggregation.
   - Created a calculated column for **Profit Margin** using the formula: `Profit / Sales`.
6. **Whitespace & Text Trimming**: Removed leading/trailing white spaces and standardized text values across regions and segments to ensure error-free filtering.

## Visualizations Included

- **KPI Summary** – Total sales, total profit, total orders, and profit margin
- **Donut Chart** – Profit share by customer segment
- **Bar Chart** – Top 5 states by profit margin
- **Bar Chart** – Monthly profit breakdown
- **Bar Chart** – Top 10 sub-categories by sales
- **Combo Chart** – Sales vs profit by sub-category
- **Combo Line Chart** – Monthly sales and profit trends

## Dataset Fields

- **Sales** – Total revenue generated
- **Profit** – Net monetary profit 
- **Profit Margin** – Profitability ratio (`Profit / Sales`)
- **Segment** – Customer classifications (*Consumer*, *Corporate*, *Home Office*)
- **Sub-Category** – Specific product groupings (*Chairs*, *Phones*, etc.)
- **Order Date** & **Year** – Transaction timeline (2015–2018)
- **State** – U.S. geographic locations


## Tools Used

- **Microsoft Excel** – Power Query, PivotTables, Dynamic Charts, Slicers, & Calculated Fields
- **GitHub** – Repository hosting, version control, and README portfolio documentation

## Key Business Insights

- **Regional Performance**: Profitability varies significantly across states, with top-performing states like **Montana** and **Maine** achieving the highest profit margins (over 20%).
- **Product Category Dynamics**: **Phones** and **Chairs** drive the highest total sales volume, whereas high-margin sub-categories contribute significantly to net profit despite lower sales volume.
- **Customer Segment Contribution**: The **Consumer** segment represents the largest profit share at **45%**, followed by **Corporate** at **30%**, and **Home Office** at **25%**.
- **Seasonal Profitability Trends**: Profitability follows a strong upward trajectory toward the end of the year, peaking sharply in **November** (reaching ~$9M in monthly profit).

## Strategic Recommendations

1. **Optimize Low-Margin Pricing**: Review pricing and set discount caps on high-volume, low-margin products (*Tables & Bookcases*) to prevent profit leakage.
2. **Prepare for Q4 Peak Demand**: Ramp up inventory and marketing in **September–October** to fully capture the **November** sales and profit surge.
3. **Replicate Top Regional Tactics**: Apply the high-margin operational models of top states (**Montana & Maine**, >20% margin) to lower-performing regions.
4. **Drive Consumer Retention**: Launch targeted loyalty programs for the **Consumer** segment to sustain its dominant **45%** profit contribution.
