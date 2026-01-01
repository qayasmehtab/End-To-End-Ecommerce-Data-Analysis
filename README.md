# 🛒 End-to-End E-Commerce Data Analysis Project

Welcome! This project demonstrates a **complete E-Commerce Data Analysis workflow** using Python, SQL Server, and visualization libraries like Matplotlib & Seaborn. 🚀

---

## 📁 Project Overview

This project is designed to provide insights into an e-commerce dataset including **customers, orders, payments, products, and sellers**.  
We perform **ETL (Extract, Transform, Load)**, **SQL queries**, and **data visualizations** to understand business metrics.  

### 🗂 Datasets

| File | Description |
|------|-------------|
| `customers.csv` | Customer info: IDs, city, state, ZIP codes 🏠 |
| `geolocation.csv` | Geolocation data: lat, long, city, state 📍 |
| `orders.csv` | Orders details including timestamps and statuses 📝 |
| `order_items.csv` | Items per order, including price and freight value 💰 |
| `payments.csv` | Payment info: type, installment, value 💳 |
| `products.csv` | Product details: category, dimensions, weight 📦 |
| `sellers.csv` | Seller information including city & state 🏬 |

---

## ⚙️ Workflow

1. **Load CSVs to SQL Server**  
   Using Python `pandas` and `SQLAlchemy`, we clean the data and load it into SQL Server tables.

   ```python
   df = pd.read_csv('customers.csv')
   df.to_sql('customers', con=engine, if_exists='append', index=False)

Data Cleaning & Transformation

Replace nulls with None

Clean column names (spaces -> underscores)

Map Pandas dtypes to SQL types dynamically

SQL Queries & Analysis
We perform business insights queries, for example:

Q1: Unique customer cities 🌆

Q2: Total orders in 2017 📅

Q3: Total sales per product category 💸

Q4: Percentage of orders paid in installments 💳

Q5: Customer count by state 📊

Q6: Monthly orders in 2018 📈

Q7: Average number of products per order by city 🛍️

Q8: Revenue contribution per product category 🏷️

Q9: Total revenue per seller 💰

Q10: Moving average of order values per customer 🔄

## Data Visualization
Using Matplotlib & Seaborn for friendly, insightful visuals:

sns.barplot(x='months', y='order_count', data=df, color='red')
plt.title("Orders by Month in 2018")
plt.show()

## 📊 Key Insights

Top-selling categories contribute significant revenue.

Most customers are concentrated in specific states.

The majority of payments are made in installments.

The average number of products per order varies significantly by city.

Moving average analysis shows customer buying trends over time.

## 🛠 Tech Stack

Python: Pandas, SQLAlchemy, Matplotlib, Seaborn 🐍

SQL Server: For structured data storage & querying 🖥️

Jupyter Notebook: Interactive exploration 📓
