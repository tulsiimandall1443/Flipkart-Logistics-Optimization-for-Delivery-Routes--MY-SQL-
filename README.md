# Flipkart-Logistics-Optimization-for-Delivery-Routes-MY-SQL

This project focuses on optimizing delivery routes, reducing delays, and improving shipment efficiency for Flipkart’s logistics network using SQL-based analytics. It analyzes orders, routes, warehouses, delivery agents, and shipment tracking data to uncover bottlenecks and provide data-driven recommendations.

## Tech Stack

- SQL (core analysis and reporting)
- Relational Database ( MySQL )
- PowerPoint (for presenting insights)




## Tasks Performed

### Task 1: Data Cleaning & Preparation

- Identified and deleted duplicate `Order_ID` records.
- Replaced null `Traffic_Delay_Min` with the average delay for that route.
- Converted all date columns to `YYYY-MM-DD` format using SQL date functions.
- Ensured that no `Actual_Delivery_Date` is before `Order_Date` and flagged such records.

### Task 2: Delivery Delay Analysis

- Calculated delivery delay (in days) for each order.
- Found the Top 10 delayed routes based on average delay days.
- Used window functions to rank all orders by delay within each warehouse.

### Task 3: Route Optimization Insights

For each route, calculated:
- Average delivery time (in days).
- Average traffic delay.
- Distance-to-time efficiency ratio: `Distance_KM / Average_Travel_Time_Min`.

Then:
- Identified 3 routes with the worst efficiency ratio.
- Found routes with more than 20% delayed shipments.
- Recommended potential routes for optimization.

### Task 4: Warehouse Performance

- Found the top 3 warehouses with the highest average processing time.
- Calculated total vs delayed shipments for each warehouse.
- Used CTEs to find bottleneck warehouses where processing time is greater than the global average.
- Ranked warehouses based on on-time delivery percentage.

### Task 5: Delivery Agent Performance

- Ranked agents (per route) by on-time delivery percentage.
- Found agents with on-time delivery percentage less than 80%.
- Compared average speed of top 5 vs bottom 5 agents using subqueries.
- Suggested training or workload balancing strategies for low-performing agents.

### Task 6: Shipment Tracking Analytics

- For each order, listed the last checkpoint and its timestamp.
- Found the most common delay reasons (excluding `None`).
- Identified orders with more than 2 delayed checkpoints.

### Task 7: Advanced KPI Reporting

Calculated key KPIs using SQL queries:
- Average delivery delay per region (`Start_Location`).
- On-time delivery percentage:  
  `On-Time Delivery % = (Total On-Time Deliveries / Total Deliveries) * 100`
- Average traffic delay per route.

### Task 8: Presentation

- Prepared a PowerPoint presentation with queries and result tables for Tasks 1–7.
- Copied and pasted SQL queries and their corresponding result sets into slides.
- Ensured tables are clearly formatted and queries are concise for stakeholders.

- ## Expected Outcomes

- A reusable SQL analytics framework for logistics optimization.
- Identification of bottlenecks in routes, warehouses, and agent performance.
- Clear KPIs for delivery delay, route efficiency, and on-time performance.
- Actionable recommendations to improve delivery speed, reliability, and cost efficiency.

