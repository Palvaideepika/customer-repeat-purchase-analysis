# Customer Repeat Purchase Analysis

## 📌 Project Overview

This project analyzes customer purchasing behavior using the **Olist Brazilian E-Commerce Public Dataset**.

The main objective is to identify **first-time and repeat customers**, calculate the **repeat purchase rate**, compare **Average Order Value (AOV)** between customer segments, and generate business insights that can help improve customer retention.

The analysis was performed using **Python, SQL, Pandas, NumPy, and Matplotlib**.

---

## 🎯 Objectives

- Analyze customer purchasing behavior
- Identify first-time and repeat customers
- Calculate the repeat purchase rate
- Compare Average Order Value (AOV) between customer segments
- Perform SQL-based customer analysis
- Validate the Python results using SQL
- Create visualizations
- Generate actionable business recommendations

---

## 📊 Dataset

The project uses the **Olist Brazilian E-Commerce Public Dataset**.

Three datasets were used:

- `olist_customers_dataset.csv`
- `olist_orders_dataset.csv`
- `olist_order_payments_dataset.csv`

### Important Columns

**Customers**
- `customer_id`
- `customer_unique_id`
- `customer_city`
- `customer_state`

**Orders**
- `order_id`
- `customer_id`
- `order_status`
- `order_purchase_timestamp`

**Payments**
- `order_id`
- `payment_value`
- `payment_type`

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- SQL
- SQLite
- Matplotlib
- Google Colab
- GitHub

---

## 🔄 Project Workflow

### 1. Data Loading

The Olist CSV files were loaded using Pandas.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

customers = pd.read_csv('olist_customers_dataset.csv')
orders = pd.read_csv('olist_orders_dataset.csv')
payments = pd.read_csv('olist_order_payments_dataset.csv')

2. Data Cleaning

The order purchase timestamp was converted into datetime format.

Only orders with the status delivered were included in the repeat purchase analysis.

3. Customer Identification

Customers were identified using customer_unique_id to correctly identify unique customers across multiple orders.

4. Customer Segmentation

Customers were classified into two groups:

First-Time Customer: 1 delivered order
Repeat Customer: 2 or more delivered orders
5. Repeat Purchase Rate
The repeat purchase rate was calculated using:

Repeat Rate = Repeat Customers / Total Customers × 100
6. Average Order Value

Payment values were aggregated at the order level and used to calculate the Average Order Value for each customer segment.

7. SQL Analysis

SQL was used to:

Count orders per customer
Identify repeat customers
Calculate repeat purchase rate
Calculate Average Order Value
📈 Key Results
Metric	Result
Total Customers	93,358
First-Time Customers	90,557
Repeat Customers	2,801
Repeat Purchase Rate	3.00%
First-Time Customer AOV	160.76
Repeat Customer AOV	145.98

📊 Visualizations

The project includes visualizations comparing:

First-Time Customers vs Repeat Customers
Average Order Value by Customer Segment

These visualizations help identify customer behavior patterns and retention opportunities.

🗄️ SQL Analysis

Example SQL query used to calculate customer order counts:

SELECT
    c.customer_unique_id,
    COUNT(DISTINCT o.order_id) AS order_count
FROM customers c
JOIN orders o
    ON c.customer_id = o.customer_id
WHERE o.order_status = 'delivered'
GROUP BY c.customer_unique_id;
📁 Project Structure
customer-repeat-purchase-analysis/
│
├── README.md
├── customer_repeat_purchase_analysis.ipynb
├── customer_segment_table.csv
└── customer_repeat_purchase_analysis.csv
🚀 Conclusion

The analysis shows that the Olist customer base has a 3.00% repeat purchase rate, highlighting a strong opportunity to improve customer retention.

Personalized communication, loyalty programs, targeted offers, and product recommendations can be used to encourage customers to make additional purchases.

This project demonstrates practical skills in:

Data Cleaning
Python
Pandas
SQL
Customer Segmentation
Data Visualization
Business Analysis
Insight Generation
👩‍💻 Author

Palvai Deepika

GitHub: Palvai Deepika


### Your GitHub repository should finally contain

```text
📁 customer-repeat-purchase-analysis
│
├── 📄 README.md
├── 📓 customer_repeat_purchase_analysis.ipynb
├── 📊 customer_segment_table.csv
└── 📊 customer_repeat_purchase_analysis.csv


