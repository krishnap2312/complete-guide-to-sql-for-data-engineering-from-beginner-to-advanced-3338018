### 🟢 Beginner Level

1. **List all products** with their name and price.                              select price, name from products
2. **Retrieve all customers** who live in "New York".                            SELECT * FROM CUSTOMER   WHERE CITY LIKE 'New York'
3. **Get the names of products** that belong to the "Electronics" category.      SELECT * FROM PRODUCTS WHERE TAGS LIKE '%electronics%'
4. **Find all orders** made by customer ID `1`.                                  select * from orders where customer_id=1
5. **List all distinct cities** where customers are located.                     SELECT DISTINCT city FROM Customer
6. **Show products** that have `NULL` in the `price` field.                      SELECT * FROM PRODUCTS WHERE PRICE IS NULL
7. **Find all customers** whose name starts with "A".                            SELECT * FROM CUSTOMER WHERE CUSTOMER_NAME LIKE 'A%'
8. **List the names and suppliers** of products in the "Clothing" category.
  SELECT p.name, p.supplier FROM PRODUCTS p join categories c
  on p.category_id=c.category_id
  Where c.name='Clothing'

If you're curious to double-check all products and their categories, you can run:
SELECT p.name, c.name AS category_name
FROM products p
JOIN categories c ON p.category_id = c.category_id;

9. **Get the full details of any order** that has a rating above 4.              SELECT * FROM orders WHERE order_rating > 4

---

### 🟡 Intermediate Level

10. **Get the total number of orders** placed by each customer.
SELECT 
  c.customer_name,
  COUNT(o.order_id) AS total_orders
FROM Orders o
JOIN Customer c ON o.customer_id = c.customer_id
GROUP BY c.customer_name;


11. **Find the total amount spent** by each customer.
12. **List products** that have been ordered at least once.
13. **Find customers who have never placed an order.**
14. **Get the average rating** of each product based on the orders.
15. **List the top 3 customers** by total spending.
16. **Show total quantity ordered** for each product.
17. **Get the most recent order** for each customer.
18. **List products** that have never been ordered.
19. **Show customers** who ordered more than one product.

---

### 🔴 Advanced Level

20. **Find the most popular product** (by total quantity ordered).
21. **Calculate the delivery duration** (in hours) for each order.
22. **Rank products** by total revenue generated.
23. **Find average order rating** per category.
24. **Show each customer's first and last order date.**
25. **List the top supplier** in terms of total order revenue.
26. **Get a monthly breakdown** of total sales for 2023.
27. **Find the product with the highest rating per category.**
28. **Detect anomalies:** Find orders where total\_amount is `NULL` but quantity is not.
29. **List orders** where the order was delivered more than 48 hours after ordering.
30. **Write a query to pivot** the number of orders per customer per month.
