# Superstore Sales Performance Analysis Dashboard (v2.0)
![Superstore Dashboard Banner](https://github.com/dougieboat/Superstore-Sales-Performance-Dashboard/blob/9a6bebd9f0ca71bde23cab8c94467e99c77699c7/images/1-Superstore-Dashboard.png)

## 🚀 Introduction
This project is an advanced, interactive dashboard that transforms four years of global superstore sales data into actionable insights.

This second version of the project demonstrates a complete data workflow: starting with raw data, performing **data cleaning and normalization (2NF)**, **feature engineering**, building a **relational data model in Power Pivot**, and developing **DAX measures**. The final dashboard is built on a custom, **PowerPoint-designed wireframe** for a professional UI/UX.

> **Demo:** Watch the dashboard in action on my [LinkedIn Showcase Video](https://www.linkedin.com/posts/douglasboateng_dataanalytics-excel-dashboard-activity-7337468806228856833-z8Dx?utm_source=share&utm_medium=member_desktop&rcm=ACoAACrTIOQBtdUaWRdU8AbooB8DbPLiEQim_q4).

---

## 🛠️ Excel Skills Demonstrated
✔️ **Power Query** for data cleaning and transformation.  
✔️ **Data Normalization (2NF)** to structure data into 5 clean tables.  
✔️ **Feature Engineering** (e.g., `Delivery Duration`, `Delivery Status`).  
✔️ **Power Pivot** to create a relational data model.  
✔️ **DAX (Data Analysis Expressions)** to write complex measures for KPIs.  
✔️ **Pivot Tables** for initial analysis and slicer setup.  
✔️ **PowerPoint-to-Excel UI Design** for a custom dashboard wireframe.  
✔️ **Dynamic Charting** and **Slicers** (Year-on-Year) for interactivity.

---

## 📚 Table of Contents
[Problem Statement](#problem-statement)  
[Data Sourcing](#data-sourcing)  
[Data Transformation & Modeling](#data-transformation-and-modeling)  
[Dashboard Design (UI/UX)](#-dashboard-design-uiux)  
[Analysis and Visualization](#analysis-and-visualization)  
[Conclusion & Recommendations](#conclusion-and-recommendation)

---

## Problem Statement
This dashboard answers key business questions:
💰 What is our overall sales performance (Total, Average)?  
🌍 Which regions, segments, and cities are driving the most revenue?  
🏆 Who are our most valuable customers?  
📈 What are the seasonal trends in our sales (Month-on-Month)?  
📦 How is our product category mix distributed?  
🚚 What is our delivery performance, and how many orders are late?

---

## Data Sourcing
-   **Source:** [Kaggle Dataset – Sales Forecasting](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)
-   **Format:** CSV
-   **Dimensions:** 18 columns × 100 rows (Original)
-   **Duration:** 4 years
-   **Features:** Order Date, Region, Category, Sales, Quantity, Ship Mode, Segment, etc.

---

## Data Transformation and Modeling
This project's backbone is its robust data model, built using the following steps:
1.  **Data Cleaning (Power Query):** The raw CSV data was loaded into Power Query for initial cleaning, including removing duplicates, handling missing values, and correcting data types.
2.  **Normalization (2NF):** The data was normalized to the Second Normal Form (2NF). This reduced redundancy and improved data integrity by splitting the flat file into **5 distinct tables** (e.g., Orders, Products, Customers).
3.  **Feature Engineering:** Two new columns were engineered in the `Orders` table to provide deeper insights:
    * `Delivery Duration`: Calculates the number of days from order to shipment.
    * `Delivery Status`: Categorizes orders as 'Late', 'On Time', or 'Same Day Delivery' based on the duration.
4.  **Data Modeling (Power Pivot):** The 5 normalized tables were loaded into Excel's Power Pivot. Relationships were created between the tables to build a relational data model (a "star schema").
5.  **DAX Measures:** All key metrics were written using DAX. This includes `Total Sales`, `Average Sales`, `YoY Growth`, and more, allowing for complex and dynamic calculations.

---

## 🎨 Dashboard Design (UI/UX)
The visual layout was designed with a "UI/UX first" approach:
1.  **Wireframing (PowerPoint):** The entire dashboard layout, including placeholders for charts, KPIs, and slicers, was first designed in PowerPoint.
2.  **Importing Layout:** This PowerPoint design was saved as an image and imported into Excel as a static background.
3.  **Placing Visuals:** All the final Excel charts and slicers were built and then carefully placed *on top* of the wireframe background, ensuring a clean, pixel-perfect, and professional finish.

---

## Analysis and Visualization

### **Key Performance Indicators (KPIs)**
-   **Total Sales:** $2.26M
-   **Average Sales:** $231
-   **Total Goods Sold:** 4,922
-   **Top Performing City:** New York City

---

### **Sales by Segment and Region (Clustered Column Chart)**
| Row Labels | Central | East | South | West |
| :--- | :--- | :--- | :--- | :--- |
| **Consumer** | $258.03K | $268.02K | $183.26K | **$438.75K** |
| **Corporate** | $163.68K | $216.60K | $119.55K | $188.66K |
| **Home Office** | $92.54K | $121.74K | $93.82K | $116.89K |

> **Insight:** The **Consumer** segment in the **West** region is the single most profitable cohort, generating **$438.75K** in sales.
![Segment & Region Sales](httpsimg)

---

### **Sales Distribution per Category (Doughnut Chart)**
| Category | Count of Row ID |
| :--- | :--- |
| Furniture | 21% |
| Office Supplies | 60% |
| Technology | 19% |

> **Insight:** **Office Supplies** dominate sales *volume* at 60%, but (as seen in other charts) **Technology** and **Furniture** drive a disproportionately high amount of the *revenue*.
![Category Distribution](httpsimg)

---

### **Top 5 Customers by Sales (Bar Chart)**
| Customer | Total Sales |
| :--- | :--- |
| Adrian Barton | $14K |
| Tom Ashbrook | $15K |
| Raymond Buch | $15K |
| Tamara Chand | $19K |
| **Sean Miller** | **$25K** |

> **Insight:** A small number of high-value customers, led by **Sean Miller ($25K)**, contribute significantly to total revenue.
![Top 5 Customers](httpsimg)

---

### **Month-on-Month Sales Trend (Line Chart)**
| Month | Total Sales |
| :--- | :--- |
| Jan | $94.29K |
| Feb | $59.37K |
| ... | ... |
| Sep | $300.10K |
| Oct | $199.50K |
| **Nov** | **$350.16K** |
| Dec | $321.48K |

> **Insight:** Sales are highly seasonal. There is a significant dip in February (**$59.37K**) and a massive peak in **November ($350.16K)**, indicating a strong holiday/Q4 rush.
![Monthly Sales Trend](img)

---

### **Delivery Status Distribution (Pie Chart)**
| Status | Count of Duration Status |
| :--- | :--- |
| **Late** | **68%** |
| On Time | 27% |
| Same Day Delivery | 5% |

> **Insight:** This is a critical operational finding. An alarming **68% of all deliveries are 'Late'**, posing a significant risk to customer satisfaction.
![Delivery Status](httpsimg)

---

### **Regional Customer Distribution (Column Chart)**
| Region | Count of Row ID |
| :--- | :--- |
| Central | 2.33K |
| East | 2.71K |
| South | 1.60K |
| **West** | **3.16K** |

> **Insight:** The **West** region not only has the highest sales but also the largest customer base (**3,160 customers**), confirming its importance.
![Regional Customers](httpsimg)

---

## Conclusion and Recommendation

### 🎯 **Conclusion**
-   The Superstore generated **$2.26M** in total revenue, with an average sale of **$231**.
-   The **West** region's **Consumer** segment is the most valuable market, supported by the largest customer base.
-   Sales are driven by key customers (like Sean Miller) and are highly seasonal, peaking in **Q4 (Nov/Sep)**.
-   **Critical Operational Failure:** The most significant finding is that **68% of all deliveries are late**, which is a major logistical problem.

---

### 💡 **Recommendations**
1.  **Logistics (Urgent Priority):** Immediately investigate the root cause of the **68% 'Late' delivery rate**. This is the single biggest threat to the business and customer retention.
2.  **Marketing:** Capitalize on seasonality. Shift marketing budgets to align with the Q4 peak (Sept-Nov) and explore promotions to lift the Q1 dip (Feb).
3.  **Customer Relations:** Implement a loyalty or key account program for the **Top 5 Customers** to retain their high-value business.
4.  **Regional Strategy:** Double down on the successful **West** region. Analyze what strategies are working there and apply them to the **South** region, which lags in both sales and customer count.

---

## 📎 Quick Links
-   [Dataset on Kaggle](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)
-   [LinkedIn Showcase Video](https://www.linkedin.com/posts/douglasboateng_dataanalytics-excel-dashboard-activity-7337468806228856833-z8Dx?utm_source=share&utm_medium=member_desktop&rcm=ACoAACrTIOQBtdUaWRdU8AbooB8DbPLiEQim_q4)

---

> _Ready to explore the dashboard? Download the [Excel file](https://github.com/dougieboat/Superstore-Sales-Performance-Dashboard/blob/ba594c65297e3a59efd1a1d3aa0ddb2e895df45c/Individual_Capstone_-_Superstore_Sales.xlsx) and dive into the insights!_

---

*© 2025 Douglas Boateng | [GitHub](https://github.com/dougieboat)*