# RDAMP-Sales-Analysis
# Ace Superstore Sales Analysis – RDAMP Task 1

**Analyst**: Aqsa Shabbir
**Program**: Realcare Data Analyst Mentorship Program (RDAMP) 
**Tool Used**: Microsoft Excel (for data cleaning, transformation, analysis, and visualization)

---

## Overview

This business intelligence report explores sales performance data from Ace Superstore to answer key foundational questions related to revenue, discount patterns, regional performance, product profitability, and sales channels. The analysis supports data-driven decision-making for strategic expansion and operational optimization.

---

## 1. Data Cleaning Process

To ensure a robust and insightful analysis of the Ace Superstore Retail Dataset, we began with comprehensive data cleaning and transformation steps. These steps were necessary to address missing values, standardize inconsistent entries, and engineer features that would allow more effective business intelligence reporting. Below is a detailed account of the procedures undertaken:

### a. Column Splitting
The original dataset contained a Category column with compound values, such as 'Food - Snacks' or 'Clothing - Coats', combining broader categories and product segments. To improve granularity and support segmented analysis:
- The `Category` column was split into:
  - `Category`: Broader classification (e.g., "Food", "Clothing")
  - `Segment`: Specific product type (e.g., "Snacks", "Coats")

### b. Handling Missing Location Data
- `Region` and `Country`: Filled using mapped values from the `City` column using Store Locations(Store Locations).

### c. Imputing Missing Discounts
- `Discount`: Null values replaced with `0` (assuming no discount was applied).

### d. Category Standardization
- Many product types were redundantly classified under varied subcategories within the same theme:
- All variations such as Clothing - Bags, Clothing - Coats, etc., were unified under the single category **Clothing**.
- A similar standardization was applied for the Food category and other domains.
- For example, "Bathroom" was merged under the broader **Home** category, combining them for a more insightful and compact analysis of product performance.

### e. Feature Engineering
To enrich the dataset for margin and profitability analysis, we engineered new columns:
- Total Sales: Computed as Sales × Quantity, giving the total revenue from a transaction line.
- Margin: Calculated as Sales − Cost Price, representing per-unit profitability.
- Total Margin: Calculated as Margin × Quantity, representing the overall profit for each transaction line.
- These new columns enable further insights into revenue drivers and profit contributors by product, region, and order channel.

These steps ensured consistency and enabled profit and trend analysis.

---

## 2. Insights and Analysis

### 2.1 Regional Performance – Sales & Discounts

![Total Sales by Region](plots/total_sales_by_region.png)  
![Total Discount by Region](plots/total_discount_by_region.png)

- **Top Sales Regions**: East Midlands, Scotland, Yorkshire and the Humber, London
- **High Discounts**: North East and East of England (above 16.5%)
- **Low Sales and Low Discounts**: North Yorkshire and Wales → Possible areas for promotional focus

---

### 2.2 🛒 Best-Selling & Underperforming Products

#### ✅ Top 5 Best-Selling Products

| Product                     | Revenue (£) |
|----------------------------|-------------|
| Portable Refrigerator Freezer | 51,380.05 |
| Portable Solar Generator       | 51,174.07 |
| Electric Bike                  | 47,708.27 |
| Compact Digital Camera         | 33,252.43 |
| Compact Dishwasher             | 32,738.16 |

#### ❌ Top 5 Underperforming Products

| Product                  | Revenue (£) |
|--------------------------|-------------|
| Herb Seasoned Rice       | 17.94       |
| Flavored Rice Cakes      | 17.88       |
| Canned Black Beans       | 9.03        |
| Baking Soda              | 8.77        |
| Cinnamon Raisin Bagels  | 6.38        |

> High-performing products are primarily in electronics and durable goods.  
> Underperformers are low-cost food items with negligible revenue.

---

### 2.3 💰 Product Categories with Highest Margins

![Product Margins](plots/product_margins.png)

| Category     | Total Margin (£) |
|--------------|------------------|
| Outdoor      | 281,900.67       |
| Electronics  | 280,539.63       |
| Kitchen      | 258,795.96       |

- Focus areas for profitability: Outdoor, Electronics, and Kitchen
- Low-margin categories: Pets, Health, Fitness

---

### 2.4 🌐 Online vs In-Store Sales

![Order Mode Distribution](plots/order_mode_distribution.png)

- **Online Sales**: £1.63M (91.4%)  
- **In-Store Sales**: £153K (8.6%)

> Online is the dominant channel, highlighting the need for continued investment in digital infrastructure.

---

## ✅ 3. Conclusion & Recommendations

### Key Takeaways:
- Sales are strongest in a few key regions; others need strategic outreach.
- High-revenue products are capital equipment and electronics.
- Online channel is overwhelmingly preferred.
- Grocery items contribute minimal revenue and may be optimized or bundled.

### Recommendations:
1. **Scale high-margin categories**: Focus on Outdoor, Electronics, Kitchen.
2. **Reassess low-performing regions**: e.g., North East, Wales.
3. **Optimize product inventory**: Phase out or bundle low-profit food items.
4. **Double down on digital**: Invest in e-commerce experience and operations.
5. **Expand analysis scope**: Consider segment-based profitability tracking and forecasting.

---

## 📂 Repository Contents

- `Ace Superstore Retail Dataset.xlsx`: Cleaned dataset
- `plots/`: Contains all visualization charts used in this analysis
- `README.md`: This report in Markdown format

---

## 🔗 Submission Notes

This submission is part of the RDAMP Program's Task 1. All analysis was conducted using **Microsoft Excel**, and the report has been formatted and submitted per GitHub and program guidelines.

---

**#RDAMP** | **#SalesAnalysis** | **#ExcelAnalytics** | **#BusinessIntelligence**


