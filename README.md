<img width="1000" alt="Screen Shot 2025-04-15 at 11 09 33 AM" src="https://github.com/user-attachments/assets/cdf951b6-8bbb-41e0-8bae-cb5a775e909b" />



# Project Title: Manufacturing Performance Analytics | Power BI


Author: [Olivia Nguyen]  
Date: November 2024  
Tools Used: Power BI 

---

## 📑 Table of Contents  
I. [📌 Background & Overview](#-background--overview)  
II. [📊 Power BI Visualization](#-power-bi-visualization)  
III. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)   
IV. [📂 Dataset Description](#-dataset-description)  
V.[🧠 Design Thinking Process](#-design-thinking-process)  



## 📌 Background & Overview

### 📖 What is this project about?
The objective of this project is to analyze the manufacturing process of a bicycle manufacturer using the AdventureWorks database in Power BI. This involves ensuring timely product delivery and minimizing scrapped products. The findings will help optimize production efficiency and improve overall manufacturing performance.

  
### 👤 Who is this project for?   
The insights gained will empower the following stakeholders to make informed strategic decisions and enhance manufacturing operations:
- Data analysts & business analysts
- Production managers
- Decision-makers & executives

### ❓ Business Questions:
- How efficient is the current manufacturing process?
- What trends in production efficiency can be identified for optimization?


## 📊 Power BI Visualization
### Dashboard 1 Preview

![image](https://github.com/user-attachments/assets/6d4ef29a-8a84-4c11-9d0b-69b56ea54733)

- 🚀 **Order Volume & Work Orders** surged from 2011 to 2013, then dropped sharply in 2014 — showing scalability but also volatility in demand.  
- 🚀 **Manufacturing Time** shows a high late delivery rate (31.4%). Delays scale with demand during the time frame given, indicating systemic inefficiencies.  
- 🚀 **Top-Ordered Products**: The most frequently ordered items include BB Ball Bearing, Seat Stays, Blade, Fork End, and Chain Stays—indicating core components in high demand and potential focus areas for inventory and production optimization.  

### Dashboard 2 Preview

![image](https://github.com/user-attachments/assets/f9cb68a7-fcf5-4b49-9bc1-915df9c33ec7)

- 🚀 **Scrap Rate remains low (0.24%)**, reflecting high production quality. However, scrap slightly increases with volume, hinting at quality pressure during peak production.  
- 🚀 **Scrap rate peaks in Q3** each year, likely due to seasonal demand spikes. Overloaded capacity (limited labor or machinery) may drive inefficiencies and quality issues.  
- 🚀 **Top scrap reasons by frequency**: Seat assembly errors, oversized drill holes, paint failures, incorrect trim lengths, and thermoform temperature issues.  
- 🚀 **Top scrap reasons by cost**: Color errors, trim issues, thermoforming, and drilling — these defects have the highest financial impact, making them critical for cost reduction.
- 🚀 **Seat assembly errors** are the most frequent but **low cost**, while **color errors** are rare yet **most costly** — prioritizing color accuracy offers the greatest cost-saving potential.  


### Dashboard 3 Preview

![image](https://github.com/user-attachments/assets/af6098ca-1589-467f-9e5d-0c84463ab00a)

- 🚀 **Production Planning Gaps:** While scheduled production time remains flat, actual production time consistently exceeds it, especially in March, May, August, and September. This suggests inefficient planning and possible seasonal capacity constraints that require closer monitoring and resource adjustments.
- 🚀 **Stage-Level Time Analysis:** Stages like Frame Forming, Final Assembly, Frame Welding, and Subassembly have a higher average time spent compared to Paint and Polish-related stages. With Subassembly and Final Assembly also being the most frequently executed, they contribute to significantly high total working hours, highlighting potential bottlenecks in the production line.
- 🚀 **Product Group Performance:** The Mountain bike group experiences the highest average delivery delay, likely due to complex assembly processes or higher demand. This signals a need for targeted process improvements and possibly dedicated resources to address group-specific challenges.

- 🚀 **Production Stage Utilization:** Subassembly and Final Assembly are the most frequently executed stages, suggesting these are critical bottlenecks or resource-intensive phases in the manufacturing process.

  
## 🔎 Final Conclusion & Recommendations 

| Issue                                                                                                                                                              | Recommended Action            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------|
| Seasonal Scrap Rate Increase in Q3 – Likely due to capacity strain from high demand.                                                                               | Expand capacity during peak months (July–September) through additional shifts or outsourcing. Enhance forecasting and scheduling to better manage seasonal demand.                           |
| High Cost of Color-Incorrect Defects – Despite a low scrap rate, these defects incur significant costs.                                                            | Improve color accuracy with enhanced quality control measures and calibration tools to minimize defect-related expenses.                                                                     |
| Rising Trend of Late-Delivery Orders – Indicates capacity constraints, inefficient scheduling, and start-time delays.                                              | Optimize scheduling and enhance production start-time accuracy to mitigate delays. Strengthen raw material forecasting and supplier reliability to prevent disruptions.                      |
| Production Time Exceeding Scheduled Time – Particularly in March, May, August, and September, pointing to workload strain and poor scheduling during peak periods. | Refine production planning and adjust schedules to accommodate high-demand months more effectively.                                                                                          |
| Mountain Product Group Faces the Largest Delays – Attributed to product complexity, high demand, and supply chain challenges.                                      | Streamline production for mountain products, potentially by establishing dedicated production lines. Address supply chain bottlenecks and prioritize material allocation for mountain bikes. |
| Subassembly and Final Assembly Experience the Most Delays – Likely due to capacity overloads.                                                                      | Balance workloads across production stages and implement lean manufacturing principles. Expand capacity in subassembly and final assembly where necessary.                                   |



## 📂 Dataset Description

### 🌐 Data Source
- The Bicycle Manufacturer dataset is stored in a public Google BigQuery dataset named "adventureworks2019"
- To access the dataset, we log in to your Google Cloud Platform, navigate to the BigQuery console and search the project "adventureworks2019".

### 🔀 Data Modelling:
  There are 5 tables that we will work on it.

| Table                | Type                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Fact_Product         | Details of product sold or used in production.                                                                            |
| Fact_Workorder       | Contains order details, including product ID, scrapped products quantity, due date, start date, and end date.             |
| Dim_ScrapReason      | Reason for scrapped products.                                                                                             |
| Dim_WorkOrderRouting | Lists only on-time and late orders. Details of location, actual order and delivery time for each work order and product.  |
| Dim_Location         | Lists each stage in the production process.                                                                               |

   ![Schema_manufacturing](https://github.com/user-attachments/assets/0208da0f-b6ce-4ff8-bd7a-19f3b930ed09)


## 🧠 Design Thinking Process

### 1️⃣ Empathize

<img width="1008" alt="Screen Shot 2025-03-05 at 11 08 14 AM" src="https://github.com/user-attachments/assets/3b9bdd1a-2650-4643-9c88-a2950659d6f0" />

### 2️⃣ Define point of view

<img width="1392" alt="Screen Shot 2025-03-05 at 1 26 08 PM" src="https://github.com/user-attachments/assets/94a855f0-af37-42c0-96a0-428b17bee0ba" />

### 3️⃣ Ideate

<img width="844" alt="Screen Shot 2025-03-05 at 1 59 59 PM" src="https://github.com/user-attachments/assets/1aef1909-7b90-4bae-9624-910c6b31aa4f" />

### 4️⃣ Prototype and review  
Next, I iterated through multiple cycles of prototyping and review to refine the final result, which will be presented in the following section as a dashboard.
