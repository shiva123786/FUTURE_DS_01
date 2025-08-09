#Task - 01
# 📈 E-commerce Sales Dashboard - Power BI Project

### Task-01: Business Sales Dashboard from E-commerce Data

## 🎯 Project Objective

This project focuses on analyzing a comprehensive e-commerce dataset to derive actionable business insights. The primary goal is to identify best-selling products, uncover sales trends, and pinpoint high-revenue categories. The final deliverable is a dynamic and interactive dashboard built in Power BI designed for business stakeholders to explore data and make informed decisions.

---

## 🛠️ Tools and Technologies

* **Power BI Desktop**: Used for data modeling, transformation, and creating visualizations.
* **Power Query**: Used for all ETL (Extract, Transform, Load) operations, including data cleaning and preparation.
* **DAX (Data Analysis Expressions)**: Used for creating custom measures and calculated columns to derive key business metrics.

---

## 🔄 Project Workflow

The project followed a systematic approach from raw data to a finished dashboard:

1.  **Data Loading & Cleaning**:
    * Combined multiple raw data files (for different years) into a single master table using **Append Queries**.
    * Corrected data types for key columns like `OrderDate`, `Quantity`, and `PriceEach`.
    * Handled missing values and removed duplicates to ensure data accuracy.

2.  **Data Transformation & Enrichment**:
    * Created new columns in Power Query to enrich the dataset. The most important was a **`Revenue`** column calculated as `[Quantity] * [PriceEach]`.
    * Extracted date components (Year, Month, Quarter) from the `OrderDate` to enable time-based analysis.

3.  **Data Modeling**:
    * Designed a **star schema data model** by separating the data into a central fact table (`sales_data`) and multiple dimension tables (`Customers`, `Products`, `Orders`, etc.).
    * Established one-to-many relationships between the dimension tables and the fact table to enable powerful filtering and data slicing.

4.  **DAX Calculations**:
    * Created a dedicated `_Measures` table to store all calculations.
    * Developed key DAX measures for core KPIs, including:
        * `Total Revenue`
        * `Total Orders`
        * `Total Quantity Sold`
        * Time intelligence measures like `Year-over-Year Growth`.

5.  **Dashboard Design & Visualization**:
    * Built an interactive dashboard with a variety of visuals:
        * **Cards** for displaying high-level KPIs.
        * **Line charts** to visualize sales trends over time.
        * **Bar charts** and **Treemaps** to identify top-performing products and categories.
        * **Maps** for geographical sales analysis.
        * **Slicers** to allow for dynamic filtering by year, country, and product line.

---

## 💡 Key Insights (Example)

* **Top Performers**: The "Classic Cars" product line is the highest revenue-generating category.
* **Sales Trend**: A significant seasonal peak in sales is observed in the last quarter (October, November) of each year.
* **Geographic Analysis**: The USA is the dominant market, contributing to over one-third of the total sales.

---

## 🖼️ Dashboard Preview
<img width="1905" height="777" alt="Sales Dashboard (2)" src="https://github.com/user-attachments/assets/3915210b-0464-4064-b24a-69892db51d2b" />

---
## 🚀 How to Use

1.  Download the `.pbix` file from this repository.
2.  Open the file using Power BI Desktop.
3.  Interact with the slicers and visuals to explore the sales data from different perspectives.
