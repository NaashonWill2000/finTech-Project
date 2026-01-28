# Customer Orders Data Analysis (Pandas)

## Project Overview
This project explores and analyzes customer and order data using **Python (pandas)**.  
The goal is to demonstrate foundational data analysis techniques such as data merging, aggregation, and exploratory queries commonly used in **data analyst and quantitative roles**.

The dataset structure mimics a real-world relational environment where transactional data (orders) is linked to customer metadata.

---

## Data Sources
The analysis uses two primary datasets:

### 1. Orders Dataset
Contains transactional order-level data.
- `order_id`
- `customer_id`
- `order_purchase_timestamp`
- `order_status`
- `order_value`

### 2. Customers Dataset
Contains customer metadata.
- `customer_id`
- `customer_unique_id`
- `customer_city`
- `customer_state`

---

## Data Integration
To combine order data with customer details, a **left join** was performed using pandas `.merge()`.

```python
orders_customers = orders.merge(
    customers,
    on="customer_id",
    how="left"
)
