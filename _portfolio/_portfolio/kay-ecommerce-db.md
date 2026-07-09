---
title: "kay_ecommerce_db: Relational E-Commerce Schema"
excerpt: "Designed and implemented a 3NF relational database structure optimizing customer accounts, order routing workflows, and item inventory levels."
collection: portfolio
---

Designed, documented, and implemented a robust relational database system (`kay_ecommerce_db`) tailored for a modern fashion e-commerce platform. The project spans from theoretical conceptual design down to complex transactional SQL query optimization using MariaDB.

### Key Technical Achievements:
* **Database Normalization:** Structured the schema strictly into Third Normal Form (3NF), completely eliminating insertion, update, and deletion anomalies while maximizing data integrity.
* **Complex Data Modeling:** Developed a comprehensive Entity-Relationship Diagram (ERD) mapping relationships (1:1, 1:M, M:M) across core tables including Customers, Orders, Order_Items, and Products.
* **Advanced Query Engineering:** Formulated complex analytical scripts utilizing multi-table `INNER JOIN` operations, aggregation filters (`GROUP BY`, `HAVING`), and pattern matching.

```sql
SELECT c.customer_id, CONCAT(c.first_name, ' ', c.last_name), SUM(o.total_amount) 
FROM customers c 
INNER JOIN orders o ON c.customer_id = o.customer_id 
GROUP BY c.customer_id HAVING SUM(o.total_amount) >= 200.00;
