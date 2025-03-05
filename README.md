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








