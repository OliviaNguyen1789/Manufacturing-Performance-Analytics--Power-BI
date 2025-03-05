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

- Scrap Rate positively correlates with order quantity, peaking in 2013. 2013 peak could be linked to changes in production methods, materials, or workforce.
Next Steps: Investigate 2013 data for anomalies (new suppliers, equipment issues, process changes).

- The  most common reasons for scrap products is related to paint process.


**Manufacturing Time:**

- High Late Ratio (31.4%): Over 1 in 3 work orders are late, suggesting systematic inefficiencies rather than isolated incidents.
  
- Late Orders increase with work order volume. When production demand rises, the system struggles to scale, leading to more late orders.

Potential Causes: Poor production planning, material shortages, Overloaded production capacity—not enough machines or labor to meet demand, defects—scrap or quality issues causing delays Trend Analysis: Identify peak months or seasons with high delays.

- Subassembly and final assembly are the two production stages that are most likely to be delayed.
  --> analyze: High scrap rates leading to rework and cascading delays.

### Dashboard 2 Preview

<img width="1066" alt="Screen Shot 2025-03-05 at 2 10 24 PM" src="https://github.com/user-attachments/assets/1e7ece2b-5a74-4499-a89b-467fa7e62efb" />

- Scrap rate is especially high in the third quarter each year, suggesting seasonal factors affecting production quality.** (bổ sung do sản phẩm tăng)**
Possible Causes: Workforce Changes, Production Surge

- High-Volume Products (BB Ball Bearing, Seat Stays, Chain Stays, Blades) have low defect rates (** phải giải thích tại sao, còn các sản phẩm nào low quantity mà cao defect rate)**
--> Identify process control techniques used in these lines that could help high-defect products.
  
- Most common scrap reasons: Drill size too large, Seat assembly not as ordered, Paint process fail, Thermoform temperature issue

- Highest scrap cost by reason: Drill size too large, Thermoform temperature issue, Collar incorrect, Trim length too long. These defects result in high financial losses, making them a priority for cost reduction.

### Dashboard 3 Preview

<img width="1066" alt="Screen Shot 2025-03-05 at 2 10 57 PM" src="https://github.com/user-attachments/assets/27838d22-69e1-40e3-953f-0b69deb91c78" />

### Dashboard 4 Preview
<img width="1069" alt="Screen Shot 2025-03-05 at 2 11 20 PM" src="https://github.com/user-attachments/assets/a3396a14-914a-4193-8b76-31c4e674c9dc" />

- Actual Production Time exceeds Scheduled Time. The gap is wider in March, May, August, and September, indicating inefficient planning, unexpected disruptions, or capacity constraints.

- Nearly 30% of late-delivered orders are caused by delays in production start dates.

- Mountain Product Group has the largest late delivery ratio

Possible Causes: More Complex Manufacturing Process, Higher Demand Volume → If mountain bikes are a best-seller, backlog issues might arise.

- Late delivery ratios have increased over time across production stages, meaning the issue is systematic rather than temporary.
Possible Causes: Inefficient Resource Allocation, Delays in earlier production stages causing a snowball effect.

- Subassembly, Final Subassembly, Frame Forming & Welding have the highest late delivery ratios 
(check xem Capacity is Lower Than Actual Manufacturing Hours, Scrap Rates → delaying downstream processes)


## V. Final Conclusion & Recommendations 

The analysis has revealed some inefficiencies in manufacturing performance. The most critical problems are:

- **High Scrap Rate in Q3:** Defects peak in July–September, with major issues in drilling, seat assembly, painting, and thermoforming.
-** Late Work Orders (31.4%):** caused by capacity constraints, inefficient scheduling, and delays in production start.
- **Production time exceeds Scheduled time**: especially in March, May, August, and September, indicating seasonal workload strain.
- **Mountain product group typically has the largest late delivery date:** Possibly due to complexity, high demand, or supply chain bottlenecks.
- **Late delivery ratios are much higher for subassembly, final Subassembly stages, frame forming, and frame welding.** Reasons: capacity is much lower than actual manufacturing hours.

These issues directly impact manufacturing efficiency, delivery performance, and cost control, making them a priority for process improvement.

**Recommendations:**

1. Optimize Production Scheduling & Capacity Utilization
- Implement advanced scheduling algorithms & real-time capacity monitoring to prevent overloads.
- Analyze nad balance workload vs. capacity to match demand.

2. Reduce Scrap & Improve Quality Control
- Find out root causes of Scrap for each product to minimize defects.
- Standardize work instructions & operator training to reduce human error.
- Invest in modern technology.

3. Strengthen Supply Chain & Material Availability
- Improve raw material forecasting & supplier reliability to prevent start delays.

4. Address Production Bottlenecks (Subassembly, Welding, Frame Forming)
- Increase machine capacity → Invest in additional welding/forming equipment for high-demand stages.
- Assign skilled operators to critical bottlenecks.










   Im
  
