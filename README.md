# Blinkit-Sales-Analysis-2024-2025

An end‑to‑end Business Intelligence solution that transforms Blinkit’s raw operational and sales data into strategic insights. Powered by Power BI and MySQL, this interactive dashboard brings clarity to hundreds of thousands of transactions, revealing trends in customer behavior, inventory flows, marketing impact, and more.  

---

## 🚀 Project Objectives

- **Optimize Data Performance**  
  Shift heavy data transformations from Power BI to MySQL, reducing file size and improving report refresh speed.
- **Unify Disparate Sources**  
  Join orders, delivery, customer feedback, and marketing tables into a consolidated star schema for holistic analysis.
- **Enable Dynamic Exploration**  
  Implement bookmarks, slicers, and DAX measures to empower users to slice data by year, region, product, and more with one click.  

---

## 🔧 Methodology & Data Engineering

1. **SQL‑First ETL**  
   - Raw CSVs ingested into MySQL rather than directly into Power BI to avoid slowdowns.  
   - Created a **Master Table** by joining `orders`, `delivery_orders`, `customer_feedback`, `customer`, and related key fields.  
   - Built optimized **Fact Tables** (`inventory`, `marketing`, `master_table`) and **Dimension Tables** (`configuration`, plus separate measure tables for sales, customer, inventory, marketing).

2. **Validation & Optimization**  
   - Tested SQL views in a staging database (`test.db`) to ensure accuracy before Power BI import.  
   - Selected only necessary fields, streamlining data load and reducing model complexity.

3. **Power BI Data Modeling & DAX**  
   - Imported three MySQL‑backed tables (`mastertable`, `inventorytable`, `marketingtable`).  
   - Maintained a **star schema** with clear relationships for performant querying.  
   - Developed advanced DAX measures (Year, Prev Year, YTD Month, Area) using the SQL‑prepared configuration table.  
   - Implemented **bookmarks** and **slicer panels** across all pages for seamless, dynamic filtering.

---

## 📊 Dashboard Overview (6 Pages)

1. **Overview**  
   - Total Sales, Quantity Sold, Growth %  
   - Inventory KPIs: Available vs Damaged Stock  
   - Marketing KPIs: Clicks, Impressions, Conversion Rate  
   - Dynamic “Year”, “Area”, “Product”, “Segment”, “YTD Month” slicers  

2. **Sales Overview**  
   - Top 5 Products by Sales Value  
   - Monthly Growth Trend  
   - Area‑wise Performance Map  
   - Bookmark‑driven filters for swift comparisons  

3. **Customer Report**  
   - Total, New, Lost & Repeat Customers  
   - Feedback Scores by Segment  
   - Interactive slicers for deep drills  

4. **Feedback Analysis**  
   - Aggregated customer feedback insights  
   - Rating trends over time  
   - Complaint counts & satisfaction scores  

5. **Inventory Report**  
   - Metrics: Total Received, Stock Available, Damaged Units  
   - Trends in stock movement  
   - Precision visuals powered by SQL‑backed data  

6. **Marketing Report**  
   - Monthly Ad Spend vs Impressions  
   - ROI by Marketing Channel  
   - Unified slicers & bookmarks for consistent UX  

---

## 🌟 Key Outcomes & Takeaways

- **Performance Gains**: By offloading transformations to MySQL, report refresh times dropped significantly, ensuring near real‑time insights.
- **Scalable Model**: Star schema design and optimized tables support future data growth and additional data sources.  
- **User‑First Design**: Bookmarks and slicer panels create an intuitive, “one‑click” exploration experience for analysts and decision‑makers.  
- **Forecast‑Ready**: Incorporated 2025 forecasted data to help teams anticipate trends and act proactively.

---

## 📂 Repository Contents

├── Blinkit_Project_Documentation.docx – Detailed project write‑up
├── Blinkit_Dashboard.pbix – Power BI report file
├── SQL_Scripts/ – MySQL scripts for ETL and view definitions
├── assets/ – Icons, backgrounds, and design files
└── README.md – Project overview and usage instructions

---

> “In every byte of data lies a story waiting to guide strategic action. This dashboard is your compass through Blinkit’s dynamic delivery landscape.”  

