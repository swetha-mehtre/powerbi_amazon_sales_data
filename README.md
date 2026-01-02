# 📊 Amazon Products Sales Analysis

[![Power BI](https://img.shields.io/badge/Data_Visualization-Power_BI-yellow)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/Analytics-DAX-blue)](https://learn.microsoft.com/en-us/dax/)

## 🌟 Project Overview
This project features an end-to-end **Power BI Dashboard** that analyzes Amazon sales data. It focuses on tracking revenue performance, understanding product popularity through customer feedback, and identifying seasonal trends for inventory forecasting.

### 🔗 Portfolio Links
* **Video Walkthrough:** [YouTube Demo](https://youtu.be/eQliphTVUf8?feature=shared)
* **Professional Profile:** [LinkedIn - Swetha Mehtre](https://www.linkedin.com/in/swetha-mehtre-6619442a9)
* **Contact:** swethamehtre@gmail.com
* alternative email:mehtreswetha@gmail.com

---

## 🚀 Business Requirements
The dashboard addresses the following key business problems:
1.  **Sales Performance:** Monitoring Year-to-Date (YTD) and Quarter-to-Date (QTD) revenue.
2.  **Customer Insights:** Correlating sales volume with the number of reviews to gauge product sentiment.
3.  **Inventory Planning:** Identifying high-growth months to ensure stock availability.

---

## 🛠️ Data Architecture & Modeling
The project utilizes a **Star Schema** to ensure optimized performance and accurate time-intelligence calculations.

* **Fact Table:** `Amazon_Data` (Sales transactions, prices, shipments, and reviews).
* **Dimension Table:** `Date Table` (Custom table for Year, Quarter, Month, and Week analysis).
* **Relationship:** One-to-Many ($1:*$) relationship between `Date Table[Date]` and `Amazon_Data[Order Date]`.

---

## 📈 Key DAX Measures
The following core measures were developed for the executive summary:

| Metric | DAX Formula |
| :--- | :--- |
| **YTD Sales** | `TOTALYTD(SUM(Amazon_Data[Price(Dollar)]), 'Date Table'[Date])` |
| **QTD Sales** | `TOTALQTD(SUM(Amazon_Data[Price(Dollar)]), 'Date Table'[Date])` |
| **YTD Reviews** | `TOTALYTD(SUM(Amazon_Data[Number of reviews]), 'Date Table'[Date])` |
| **Month Name** | `FORMAT('Date Table'[Date], "MMM")` |

---

## 🖥️ Dashboard Insights
### **1. Performance KPIs**
* **Total Revenue:** Tracked at $28.44K (YTD).
* **Customer Engagement:** High correlation between sales peaks and review volume (6.77K reviews YTD).

### **2. Trend Analysis**
* **Seasonal Peak:** A major sales surge is visible in **November**, likely driven by holiday shopping and Black Friday events.
* **Weekly Granularity:** The "Sum of Price by Week" chart allows for identifying specific high-traffic weeks for better supply chain management.

### **3. Product Deep Dive**
* **Top 5 Products:** Identified by sales revenue vs. review volume to see which products are the most profitable versus the most discussed.

---

## 🕹️ How to Use
1.  **Filters:** Use the sidebar slicers to filter data by **Product Category** or **Quarter**.
2.  **Cross-Filtering:** Click on any bar or line chart segment to see the entire dashboard update dynamically for that specific data point.

---

## 🏁 Conclusion
The analysis reveals that the **last quarter of the year** is the most critical for revenue generation. By focusing inventory and marketing efforts on the top 5 products identified in this dashboard, the business can significantly maximize its ROI.

---
*Developed by Swetha Mehtre - 2025*
