# Project Title: Bicycle Manufacturer dataset - Manufacturing Performance Analytics | Power BI


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
The insights gained will empower the following stakeholders to make informed strategic decisions and enhance manufacturing operations:
- Data analysts & business analysts
- Production managers
- Decision-makers & executives

### Business Questions:
- Why does the company fail to deliver these products on time?
- What strategies can be implemented to minimize scrapped products?
  

## II. Dataset Description

- Source: The Bicycle Manufacturer dataset is stored in a public Google BigQuery dataset named "adventureworks2019"
  To access the dataset, we log in to your Google Cloud Platform, navigate to the BigQuery console and search the project "adventureworks2019".
  
- Data Modelling:
  There are 5 tables that we will work on it.

| Table                | Type                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Fact_Product         | Details of product sold or used in production.                                                                            |
| Fact_Workorder       | Contains order details, including product ID, scrapped products quantity, due date, start date, and end date.             |
| Dim_ScrapReason      | Reason for scrapped products.                                                                                             |
| Dim_WorkOrderRouting | Lists only on-time and late orders. Details of location, actual order and delivery time for each work order and product.  |
| Dim_Location         | Lists each stage in the production process.                                                                               |

   ![Schema_manufacturing](https://github.com/user-attachments/assets/0208da0f-b6ce-4ff8-bd7a-19f3b930ed09)


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

![BI_1 (1)](https://github.com/user-attachments/assets/5581579c-f6b2-46ec-8938-70fb8d87cb50)

**🚀 Scrap rate:**

- Scrap Rate is Low (0.24%), indicating an efficient production process. However, even small percentages can be costly, especially if high-value products are affected.

- Scrap rate is especially high in the third quarter each year, suggesting seasonal factors affecting production quality.

- The  most common reasons for scrap products is related to paint process.

**🚀 Manufacturing Time:**

- High Late Ratio (31.4%): Over 1 in 3 work orders are late, suggesting systematic inefficiencies rather than isolated incidents.
  
- Late Orders increase with work order volume. When production demand rises, the system struggles to scale, leading to more late orders.
Potential Causes: Poor production planning, material shortages, Overloaded production capacity—not enough machines or labor to meet demand, defects—scrap or quality issues.

- Subassembly and final assembly are the two production stages that are most likely to be delayed.
  

### Dashboard 2 Preview

![BI_2 (1)](https://github.com/user-attachments/assets/d546ae97-cfd5-4bde-8754-b5de9b7d8110)

- 🚀 Scrap Rate shows a positive correlation with order quantity, consistently peaking in the third quarter each year, with a notable surge in 2013. This increase may stem from overloaded production capacity—insufficient machines or labor to meet rising demand, leading to inefficiencies and higher scrap rates.
  The 2013 peak could be attributed to shifts in production methods, material changes, or workforce adjustments, potentially disrupting efficiency and quality control.

- 🚀 High-Volume Products (BB Ball Bearing, Seat Stays, Chain Stays, Blades) have low defect rates  --> Identify process control techniques used in these lines that could help high-defect products.
  
- 🚀 Most common reasons of high scrap rate:  Seat assembly not as ordered, Drill size too large, Paint process fail name, Trim length too long, Thermoform temperature issue

- 🚀 Highest scrap cost by reason: Color incorrect, Trim length too long, Thermoform temperature issue, Drill size too large. These defects result in high financial losses, making them a priority for cost reduction.

- 🚀 Remarkably, while seat assembly errors contribute the most to scrap rate, their financial impact (cost) is minimal. In contrast, color incorrect defects — despite their low scrap rate — incur the highest costs. Given this, minimizing scrap caused by color incorect should be the top priority for cost reduction.


### Dashboard 3 Preview

![Bi_3 (1)](https://github.com/user-attachments/assets/1d99efe2-c814-46aa-bb94-bd5d83d3396d)

- 🚀 The late ratio has shown an upward trend from 2011 to 2014, rising from 29.47% in 2011 to 36.65% in 2014. In general, late orders rise with work order volume, suggesting that the system struggles to scale due to factors such as material shortages and overloaded production capacity.

- 🚀 Scheduled Time remained constant from 2011 to 2014, while Actual Production Time showed a slight decline. Notably, Actual Production Time consistently exceeds Scheduled Time, with the gap widening in March, May, August, and September. This pattern suggests inefficiencies in planning, unexpected disruptions, or capacity constraints affecting production efficiency.

- 🚀 Nearly 30% of late-delivered orders are caused by delays in production start dates.

- 🚀 The Mountain Product Group having the largest average number of days late in delivery indicates a systemic issue that needs targeted attention. 
  Possible Causes: More Complex Manufacturing Process, Higher Demand Volume → If mountain bikes are a best-seller, backlog issues might arise.


### Dashboard 4 Preview

![BI_4 (1)](https://github.com/user-attachments/assets/78e91896-375d-4a3b-aad2-5b8ec4d94705)

- 🚀 Late delivery ratios have increased over time across production stages, meaning the issue is systematic rather than temporary.
  Possible Causes: Inefficient Resource Allocation, Delays in earlier production stages causing a snowball effect.

- 🚀 Currently, capacity is almost evenly distributed across production stages, creating imbalances where stages requiring more production time face shortages, while others have excess capacity. As a result, Subassembly, Final Subassembly, and Frame Forming & Welding experience the highest late delivery ratios due to insufficient capacity in these critical stages.
  
- 🚀 In the production stages, Frame Forming and Frame Welding incur significantly higher costs, with production expenses being twice as high as those in the remaining stages.


## V. Final Conclusion & Recommendations 

The analysis has revealed some inefficiencies in manufacturing performance. The most critical problems are:

- **Seasonal Scrap Rate Increase in Q3**: Defects surge from July to September, likely due to capacity strain from high demand.
- **High Cost of Color Incorrect Defects**: Despite low scrap rate, color-related defects incur the highest costs, making their reduction a key priority.
- **Rising Late Work Orders (31.4%) Show an Ongoing Trend**: Increasing trend of late orders points to capacity constraints, inefficient scheduling, and start-time delays.
- **Production Time Exceeds Scheduled Time**: Especially in March, May, August, and September, suggesting workload strain and poor scheduling during peak periods.
- **Mountain Product group faces the largest Delay**: Likely caused by product complexity, high demand, and potential supply chain issues.
- **Subassembly and Final Assembly Experience Most Delays**: These stages are most often delayed, potentially due to capacity overloads.

These issues directly impact manufacturing efficiency, delivery performance, and cost control, making them a priority for process improvement.

### Recommendations:

1. Reduce Scrap products and Scrap cost
   - Enhance color accuracy with better quality control and calibration tools to reduce cost of defects.
   - Increase capacity during peak months (July–September) with extra shifts or outsourcing.
   - Improve forecasting and scheduling to better manage seasonal demand.

2. Optimize Production Scheduling
  - Optimize scheduling and improve production start timing to avoid delays.
  - Refine production planning and adjust schedules for high-demand months.
  - Improve raw material forecasting & supplier reliability to prevent start delays

3. Optimize Capacity Utilization
  - Balance workloads across stages and apply lean manufacturing principles.
  - Expand capacity where needed and consider adding shifts or equipment.
  - Increase capacity in subassembly and final assembly.

4. Address Production Bottlenecks (Mountain Product Group)
  - Streamline production for mountain products, potentially with dedicated lines.
  - Address supply chain bottlenecks and prioritize materials for mountain bikes.


