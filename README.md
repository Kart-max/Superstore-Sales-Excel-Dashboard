# Superstore-Sales-Excel-Dashboard
Interactive Excel dashboard analyzing 10k+ rows of Superstore sales data. Showcases data cleaning, custom feature engineering with IF logic, and dynamic visualizations. Features interconnected Pivot Tables and Charts controlled by Slicers to filter revenue trends by year and customer segment.
# Superstore Sales Performance Dashboard

**Author:** Kartikeya Rai 
**Tools Used:** Microsoft Excel
**Target Role:** Data Analyst Intern

## Project Objective
The goal of this project is to analyze a raw retail dataset to uncover sales trends and customer behavior. It serves as a comprehensive demonstration of core Excel skills required for data analysis, including data cleaning, feature engineering, and interactive visualization.

## Dataset
* **Source:** Kaggle (Superstore Sales Forecasting Dataset)
* **Size:** 10,000+ rows
* **Note:** This specific dataset iteration focuses strictly on revenue and sales volume.

## Data Preparation & Cleaning
Before visualization, the raw `.csv` data underwent the following transformations:
* **Quality Assurance:** Handled formatting anomalies (e.g., legacy date format bugs) and auto-fitted columns for proper numeric rendering. Checked for duplicate records.
* **Date Extraction:** Used the `=YEAR()` and `=TEXT( , "mmm")` functions to extract specific **Order Year** and **Order Month** columns for time-series filtering.
* **Feature Engineering:** Created a custom **Order Size** classification using nested logic: `=IF([Sales]>500, "High Value", "Standard")` to segment revenue streams.

## Dashboard Components
The final dashboard is built on an underlying engine of dynamic Pivot Tables, featuring three primary visualizations:
1. **Sales by Category (Bar Chart):** Highlights which product categories drive the most revenue.
2. **Order Size Breakdown (Pie Chart):** Visualizes the proportion of revenue coming from "High Value" vs. "Standard" transactions.
3. **Sales by Region (Column Chart):** Compares geographical performance across the US.

### Interactivity
The dashboard includes **Slicers** for `Order Year` and `Segment` (Consumer, Corporate, Home Office). These slicers are globally connected to all Pivot Tables via *Report Connections*, allowing the user to click a year or segment and instantly filter the entire dashboard.

## How to Use
1. Download the `Superstore_Sales_Dashboard.xlsx` file from this repository.
2. Open the file in Microsoft Excel (Desktop Version recommended for full Slicer functionality).
3. Navigate to the **"Dashboard"** tab.
4. Click the buttons on the Slicers to interact with the data!
