---
title: "kay_ecommerce_db: Relational E-Commerce Schema"
excerpt: "Designed and implemented a 3NF relational database structure optimizing customer accounts, order routing workflows, and item inventory levels."
collection: portfolio
---

Designed, documented, and implemented a robust relational database system (`kay_ecommerce_db`) tailored for a modern fashion e-commerce platform. The project applies database systems analysis principles to build clean data models for transactional business management.

### Key Technical Focus Areas:
* **Database Normalization:** Structured the schema strictly into Third Normal Form (3NF), completely eliminating insertion, update, and deletion anomalies while maintaining absolute functional dependencies.
* **Data Modeling & Integrity:** Developed a comprehensive Entity-Relationship Diagram (ERD) mapping relationships across core business tables including Customers, Orders, Order_Items, and Products.
* **Advanced Analytical Queries:** Formulated complex query scripts utilizing multi-table `INNER JOIN` operations, aggregation filters (`GROUP BY`, `HAVING`), and pattern matching to identify high-value customer accounts.

```sql
SELECT c.customer_id, CONCAT(c.first_name, ' ', c.last_name) AS customer_name, SUM(o.total_amount) 
FROM customers c 
INNER JOIN orders o ON c.customer_id = o.customer_id 
GROUP BY c.customer_id HAVING SUM(o.total_amount) >= 200.00;

### Project Video Walkthrough
Click the video below for a live, technical demonstration of the system architecture, database normalization choices, and runtime performance tracking.

[![Watch the video](https://img.youtube.com/vi/YOUR_VIDEO_ID_HERE/maxresdefault.jpg)](https://youtu.be/PZr8-hkPwmE)
