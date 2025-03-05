# -Power-BI-Manufacturing-Analytics


Author: [Uyen Nguyen]  
Date: November 2024  
Tools Used: Power BI 

---

## 📑 Table of Contents  
I. [Introduction](#i-introduction)  
II. [Dataset Description](#ii-dataset-description)  
III.[Design Thinking Process](#iii-design-thinking-process)  
IV.[Power BI Visualization](#iv-power-bi-visualization)  
V. [Final Conclusion & Recommendations](#v-final-conclusion--recommendations)

## I. Introduction

Based on the AdventureWorks database, this project analyzes the manufacturing process of a bicycle manufacturer using Power BI.
### The objective:
- Ensure products are delivered on time.
- Minimize scrapped products.
  
### Stakeholders: 
The insights gained will empower the following stakeholders to make informed strategic decisions and enhance overall business operations:
- Data analysts & business analysts
- Production managers
- Decision-makers & executives

### Business Questions:
- Which products are frequently delivered late?
- Why does the company fail to deliver these products on time?
- What strategies can be implemented to minimize scrapped products?


## II. Dataset Description

- Source: The Bicycle Manufacturer dataset is stored in a public Google BigQuery dataset named "adventureworks2019"
- Data Structure:
  There are 5 tables that we will work on it.

| Table                | Type                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Fact_Product         | Details of product sold or used in production.                                                                            |
| Fact_Workorder       | Contains order details, including product ID, scrapped products quantity, due date, start date, and end date.             |
| Dim_ScrapReason      | Reason for scrapped products.                                                                                             |
| Dim_WorkOrderRouting | Lists only on-time and late orders. Details of location, actual order and delivery time for each work order and product.  |
| Dim_Location         | Lists each stage in the production process.                                                                               |


-  Data relationships: (bổ sung data modelling)





## III. Design Thinking Process

### 1. Empathize

<img width="1008" alt="Screen Shot 2025-03-05 at 11 08 14 AM" src="https://github.com/user-attachments/assets/3b9bdd1a-2650-4643-9c88-a2950659d6f0" />

### 2. Define point of view

<img width="1392" alt="Screen Shot 2025-03-05 at 1 26 08 PM" src="https://github.com/user-attachments/assets/94a855f0-af37-42c0-96a0-428b17bee0ba" />

### 3. Ideate

<img width="844" alt="Screen Shot 2025-03-05 at 1 59 59 PM" src="https://github.com/user-attachments/assets/1aef1909-7b90-4bae-9624-910c6b31aa4f" />


Next, I proceeded with Step 4 - Prototype and Review multiple times and achieved the final result, which will be presented in the following section as a dashboard.



## IV. Power BI Visualization
### Dashboard 1 Preview

<img width="1059" alt="Screen Shot 2025-03-05 at 2 09 01 PM" src="https://github.com/user-attachments/assets/edffcfd9-e0a5-43c1-9b07-bbc41b596d32" />

**Scrap rate:**

- Scrap Rate is Low (0.24%), indicating an efficient production process. However, even small percentages can be costly, especially if high-value products are affected.
Next Steps: Instead of focusing on reducing overall scrap, prioritize the most expensive or most frequent defects (e.g., paint process issues).

- Scrap Rate positively correlates with Order Quantity,peaking in 2013. 2013 peak could be linked to changes in production methods, materials, or workforce.
Next Steps: Investigate 2013 data for anomalies (new suppliers, equipment issues, process changes).

- The  most common reasons for scrap products is related to paint process.


**Manufacturing Time:**

- High Late Ratio (31.4%): Over 1 in 3 work orders are late, suggesting systematic inefficiencies rather than isolated incidents.
  
- Late Orders Increase with Work Order Volume. When production demand rises, the system struggles to scale, leading to more late orders.

Potential Causes: Poor production planning, material shortages, Overloaded production capacity—not enough machines or labor to meet demand, defects—scrap or quality issues causing delays Trend Analysis: Identify peak months or seasons with high delays.

- Subassembly and final assembly are the two production stages that are most likely to be delayed.
  --> analyze: High scrap rates leading to rework and cascading delays.

### Dashboard 2 Preview

<img width="1066" alt="Screen Shot 2025-03-05 at 2 10 24 PM" src="https://github.com/user-attachments/assets/1e7ece2b-5a74-4499-a89b-467fa7e62efb" />

- Scrap rate is especially high in the third quarter each year, suggesting seasonal factors affecting production quality.** (bổ sung do sản phẩm tăng)**
Possible Causes: Workforce Changes, Production Surge

- High-Volume Products (BB Ball Bearing, Seat Stays, Chain Stays, Blades) have Low Defect Rates (** phải giải thích tại sao, còn các sản phẩm nào low quantity mà cao defect rate)**
--> Identify process control techniques used in these lines that could help high-defect products.
  
- Most Common Scrap Reasons: Drill size too large, Seat assembly not as ordered, Paint process fail, Thermoform temperature issue

- Highest Scrap Cost by Reason: Drill size too large, Thermoform temperature issue, Collar incorrect, Trim length too long. These defects result in high financial losses, making them a priority for cost reduction.

### Dashboard 3 Preview

<img width="1066" alt="Screen Shot 2025-03-05 at 2 10 57 PM" src="https://github.com/user-attachments/assets/27838d22-69e1-40e3-953f-0b69deb91c78" />

### Dashboard 4 Preview
<img width="1069" alt="Screen Shot 2025-03-05 at 2 11 20 PM" src="https://github.com/user-attachments/assets/a3396a14-914a-4193-8b76-31c4e674c9dc" />

- Actual Production Time Exceeds Scheduled Time. The gap is wider in March, May, August, and September, indicating inefficient planning, unexpected disruptions, or capacity constraints.

- Nearly 30% of late-delivered orders are caused by delays in production start dates.

- Mountain Product Group Has the Largest Late Delivery Ratio

Possible Causes: More Complex Manufacturing Process, Higher Demand Volume → If mountain bikes are a best-seller, backlog issues might arise.

- Late Delivery Ratios Have Increased Over Time Across production stages
Interpretation: The late delivery problem is worsening, meaning the issue is systematic rather than temporary.
Possible Causes:
Capacity Constraints Not Scaling with Demand → As orders increase, production is struggling to keep up.
Inefficient Resource Allocation → Machines and labor may not be optimally distributed.
Growing Backlogs & Bottlenecks → Delays in earlier production stages causing a snowball effect.
Next Steps:
Trend Analysis: Is the increase in late deliveries proportional to order growth?
Resource Utilization Analysis: Are key production areas overburdened while others have idle time?
Work Order Flow Optimization: Identify stages with excessive queue times.
5. Subassembly, Final Subassembly, Frame Forming & Welding Have the Highest Late Delivery Ratios
Interpretation: These are the biggest bottlenecks causing production delays.
Reason: Capacity is Lower Than Actual Manufacturing Hours → These stages require more time than available resources can handle.
Possible Causes:
Insufficient Machines or Skilled Labor → Too few workstations or workers for demand levels.
High Rework & Scrap Rates → Defective components forcing rework and delaying downstream processes.
Long Setup & Changeover Times → Inefficiencies in switching between different product batches.
Next Steps:
Assess machine capacity vs. work order volume at these stages.
Measure rework rates—are quality issues making delays worse?
Investigate setup times—can production runs be optimized for efficiency?


👉🏻 Insert Power BI dashboard screenshots here

📌 Analysis 3:

Observation: Describe trends, key metrics, and patterns.
Recommendation: Suggest actions based on insights.

## V. Final Conclusion & Recommendations 

This analysis provides valuable insights into sales performance across products and regions, inventory management, and customer retention. It enables the bicycle manufacturer to identify strengths and weaknesses, allowing them to leverage their strengths and minimize weaknesses to enhance overall business performance.

**Recommendations:**

- Analyze the strategies that led to success in Territories 4, 6, and 1, and replicate them in underperforming regions to boost overall sales.
- Reevaluate the effectiveness of promotional campaigns, such as the Seasonal Discounts for Helmets, to ensure they drive sales without causing a disproportionate increase in discount costs.
- Prioritize customer retention by enhancing the customer experience and providing additional value after the initial purchase to reduce churn.
- Focus on improving demand forecasting and optimizing just-in-time inventory cycles to reduce stock imbalances, lower holding costs, and avoid stockouts of high-demand items.
- Conduct a thorough analysis to identify the causes of the sharp sales decline in Q2 2014 and address pending orders to implement prompt and effective solutions.


For the first question: Our results show that 
•	Actual production time is much higher than scheduled production time;
•	Capacity is much lower than actual manufacturing hours.
That is why we recommend 2 solutions: 
•	Firstly, Adjust production planning based on actual situation.
•	Then the company could consider to  Invest in modern technology to improve production capacity.
For the second question, we suggets that:
The company could Invest in modern technology, and Improving working skills for employees to minimize the scrapped product.








