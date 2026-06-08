# SQLite Sales Analysis Demo (Python + In‑Memory Database)

This project builds a small in‑memory SQLite database to simulate 90 days of product sales. It creates `products` and `orders` tables, loads sample data, and runs a series of analytical SQL queries to explore totals, averages, revenue, category performance, popular products, and subquery‑based insights.

# What This Script Does
- Creates an in‑memory SQLite database
- Defines `products` and `orders` tables with a foreign key relationship
- Inserts sample product data and 90‑day order history
- Runs SQL queries to calculate:
  - Total orders
  - Total units sold
  - Average order quantity
  - Product price range
  - Revenue by category (JOIN + GROUP BY)
  - Popular products (HAVING)
  - Above‑average priced products (subquery)
  - Products never ordered (subquery with NOT IN)

# Table Structure
# Products
- id (PK)
- name
- category
- price

# Orders
- id (PK)
- product_id (FK → products.id)
- quantity
- order_date

# Key Queries Demonstrated
- Aggregates: `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- Grouping: `GROUP BY`, `HAVING`
- Joins: `INNER JOIN` on product relationships
- Subqueries: scalar subqueries and `NOT IN` lists
- Sorting and formatting results

# Example Insights Produced
- Total quarterly orders and units sold
- Average units per order (rounded)
- Revenue by category, sorted highest to lowest
- Products ordered at least twice
- Products priced above the overall average
- Products that never appeared in any order

# Running the Script
SQLite is built into Python. Just run:

```bash
python3 your_script_name.py
