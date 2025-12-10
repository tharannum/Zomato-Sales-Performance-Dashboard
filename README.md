# Zomato-Sales-Performance-Dashboard
![overview](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/Overview.jpg)
  
## **Executive Summary**

Zomato, a leading online food delivery and restaurant discovery platform, collects extensive data on orders, customers, partner restaurants, delivery locations, and operational performance. However, much of this data remains underutilized for strategic decision-making.

This Business Intelligence project analyzes Zomato’s sales and operational dataset using Power BI to uncover key insights across revenue trends, customer patterns, restaurant performance, delivery behavior, and refund/return issues. The goal is to deliver **clear, data-driven insights** that can improve Zomato’s commercial success, restaurant partnerships, and customer satisfaction.

The analysis includes:

* **Sales Trends Analysis**: Revenue, order volume, and average order value (AOV) trends over time.
* **Restaurant-Level Performance**: Identifying top vs. lagging restaurants and cuisine performance patterns.
* **Customer Behavior Insights**: Repeat purchase rates, order frequency, and delivery time impact.
* **Refund & Cancellation Patterns**: Highlighting inefficiencies and operational bottlenecks.
* **Regional Breakdown**: Comparing city-wise and zone-wise food delivery performance.

An interactive Power BI dashboard has been built to visualize these insights and support data-driven decision-making for business, operations, marketing, and leadership teams.

### Overall Performance Dashboard 
The Overall Performance Dashboard provides a high-level summary of all key business indicators in a single view. This page acts as the central hub for stakeholders to quickly understand how the business is performing across sales, customers, product categories, and operational metrics.

You can find the Power BI Dashboard HERE: https://acrobat.adobe.com/id/urn:aaid:sc:ap:1d9ad110-78c6-4715-b8e4-7903e14ed6a7 

---

# 🗂️ **1. Project Overview**

The purpose of this Power BI project is to convert raw food delivery data into a comprehensive, insight-driven dashboard that helps Zomato understand:

* How sales are trending over time
* Which restaurants and cuisines drive the most revenue
* How customer ordering behavior is evolving
* Where refund and cancellation issues occur
* Which regions contribute most to sales
* What operational factors influence delivery efficiency

This dashboard allows both technical and non-technical stakeholders to explore real-time KPIs, identify problem areas, and take informed actions to grow revenue and improve the customer experience.

---

# 🗃️ **2. Data Description**

### **Dataset Source**

The project uses cleaned Excel files exported from Zomato’s sales and operations system.

### **Included Fields**

* **Order Details**: Order ID, date, time, restaurant ID, food category, quantity, price
* **Restaurant Information**: Restaurant name, cuisine, ratings, city/zone
* **Customer Data**: Customer ID, location, repeat orders
* **Operational Metrics**: Refund status, delivery time, cancellation reasons

### **Data Preparation (Power Query)**

In Power Query, the following steps were performed:

* Removed duplicates and invalid entries
* Standardized date/time formats
* Cleaned refund and cancellation columns
* Split and merged columns for better modeling
* Corrected null restaurant IDs using mapping logic
* Created new calculated fields (AOV, Delivery Duration Group, Refund Flag)

### **Data Model (Star Schema)**

The data was modeled using:

* **Fact Table**: Orders_Fact (contains transaction-level data)
* **Dimensions**:

  * Dim_Date
  * Dim_Restaurant
  * Dim_Customer
  * Dim_Location

Relationships were created using primary/foreign keys such as customer_id, restaurant_id, and date_id.

---

# 📈 **3. Analysis Performed**

The following analytical components were built in Power BI:

### **Power Query Transformations**

* Cleaning and shaping the dataset
* Creating custom columns (Month, Quarter, Order Sessions, Delivery Speed Category)

### **DAX Measures**

* Total Revenue
* Total Orders
* Average Order Value (AOV)
* Refund Rate
* Customer Repeat Rate
* YoY Revenue Growth
* MTD & QTD calculations
* Rolling 4-week and 12-week averages

### **Visualizations**

* KPIs (Revenue, Orders, AOV, Refund %)
* Line charts (Sales Over Time)
* Clustered bar charts (Top Restaurants / Cuisines)
* Stacked column charts (Regional Sales Contribution)
* Matrix tables (Category vs. City)
* Slicers (Date, Category, City, Restaurant)
* Decomposition tree for root-cause analysis
* Drillthrough pages for restaurant-level details

These visuals help uncover performance patterns and support decision-making.

---

# ❓ **4. Business Questions Answered**

The dashboard answers the following key questions:

1. **What are the monthly and quarterly sales trends?**
2. **Which restaurant partners contribute the most to sales and orders?**
3. **Which food categories perform best?**
4. **Which restaurants or cuisines are lagging?**
5. **What is the refund and cancellation rate, and what causes it?**
6. **How do different regions/cities perform across KPIs?**
7. **What is the average delivery time and how does it affect customer satisfaction?**
8. **Which customers are repeat buyers?**

---

# 🔍 **5. Insights & Interpretation**

Below are examples of key insights derived from the dashboard.

---

### **Insight 1 — Revenue Trend Decline After Peak Period**

Revenue peaked in **2018** but declined steadily for the next three months, dropping **2020**.

**![Year Sales Trend](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/Sales%20by%20Year.jpg)**

---

### **Insight 2 — Top 5 city Contribute 62% of Total Revenue**

A small group of high-performing restaurants accounts for **over half** of all sales, indicating strong dependency on a few partners.

**![Top 5 Resturants](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/city%20based%20on%20order.jpg)**

---

### **Insight 3 — Leading Category vs. Lagging Category**

* The **Leading Category (e.g., veg Combos)** grew **24%** .
* The **Lagging Category (e.g., non Veg combos)** declined **18%** in the same period.

**![Category Performance Comparison](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/different%20food.jpg)**

---

### **Insight 4 — Refund Rate Increasing**

 Increased in user **12k Gain** and **33k lost**, driven mainly by:

* Late delivery
* Order mismatch
* Restaurant unavailability
![customer](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/Gain%20And%20.jpg)

---

### **Insight 5 — City-Level Performance**

Bangalore and Hyderabad consistently deliver the highest revenue, while Tier-2 cities show strong AOV but lower order volume.
![city](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/City%20Performance.jpg)

---
### **Insight 6 - User Performance 

 Analysis shows 23-year-olds are underrepresented on our platform. We're experiencing churn among this age group, indicating a need for targeted offers to attract and retain them.
 ![age](https://github.com/tharannum/Zomato-Sales-Performance-Dashboard/blob/main/user%20performance.jpg)

---
# 📌 **6. Recommendations**

Based on the insights, here are actionable recommendations:

---

### **Sales Team**

* Strengthen partnerships with top restaurants driving 62% of revenue
* Launch retention campaigns for declining categories

---

### **Marketing Team**

* Shift marketing spend toward **high-growth categories**
* Run targeted ads for cities with high AOV but low order volume

---

### **Operations Team**

* Investigate delivery delays in regions with rising refund rates
* Standardize packaging and order verification to reduce mismatches

---

### **Leadership**

* Set quarterly KPIs to increase lagging-category sales by 10%
* Expand restaurant onboarding in high-performing cities

---

# 🛠️ **7. Skills Used**

* Power BI Desktop
* Power Query (M Language)
* DAX (Time Intelligence, KPI Measures)
* Data Cleaning & Transformation
* Business Intelligence Reporting
* Data Modeling (Star Schema)
* Data Visualization
* Analytical Storytelling
* SQL (optional — if used for preprocessing)

---

# 🏁 **8. Project Outcome**

This project delivers:

* A fully interactive **Power BI Dashboard**
* Cleaned and structured dataset with a proper star-schema model
* DAX-driven KPIs and insights
* Actionable recommendations for business growth
* A clear BI narrative understandable by both technical and non-technical users

The dashboard equips Zomato stakeholders with decision-ready insights to enhance sales performance, optimize operations, and improve customer experience.

 
