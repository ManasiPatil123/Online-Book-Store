# 📚 Online Bookstore - SQL Database Project

This project is a simple yet comprehensive SQL-based implementation of an **Online Bookstore**. It involves the design and querying of a relational database using **PostgreSQL**. The database contains essential entities such as **Books**, **Customers**, and **Orders**, with various queries demonstrating both beginner and advanced SQL operations.

## 🛠 Technologies Used

- **PostgreSQL**
- SQL (DDL, DML, and advanced queries)
- pgAdmin / SQL Shell for query execution

---

## 📂 Project Structure

- **DDL Statements**: Table creation with appropriate data types, primary and foreign key constraints.
- **DML Queries**: Insertion and retrieval queries for Books, Customers, and Orders.
- **Basic Queries**: Filtering, sorting, and aggregating data.
- **Advanced Queries**: Complex joins, grouping, and analytical operations.

---

## 🗃️ Database Schema

### `Books`
| Column         | Type              |
|----------------|-------------------|
| Book_ID        | SERIAL PRIMARY KEY|
| Title          | VARCHAR(100)      |
| Author         | VARCHAR(100)      |
| Genre          | VARCHAR(50)       |
| Published_Year | INT               |
| Price          | NUMERIC(10,2)     |
| Stock          | INT               |

### `Customers`
| Column       | Type              |
|--------------|-------------------|
| Customer_ID  | SERIAL PRIMARY KEY|
| Name         | VARCHAR(100)      |
| Email        | VARCHAR(100)      |
| Phone        | VARCHAR(15)       |
| City         | VARCHAR(50)       |
| Country      | VARCHAR(150)      |

### `Orders`
| Column       | Type               |
|--------------|--------------------|
| Order_ID     | SERIAL PRIMARY KEY |
| Customer_ID  | INT (Foreign Key)  |
| Book_ID      | INT (Foreign Key)  |
| Order_Date   | DATE               |
| Quantity     | INT                |
| Total_Amount | NUMERIC(10,2)      |

---

## 🔍 SQL Queries Included

### 📌 Basic Queries
- List books in a specific genre
- Find books published after a certain year
- View customers from a specific country
- Filter orders by date range
- Calculate total stock and revenue
- Retrieve the most/least expensive book
- List all unique genres

### 🔎 Advanced Queries
- Total books sold per genre and author
- Most frequently ordered book
- Top spending customer
- Cities with customers spending over $30
- Customers with multiple orders
- Remaining stock after orders
- Top 3 expensive books in "Fantasy" genre
- Average price of "Fantasy" books

---

## 💡 Sample Advanced Query

sql
-- Find the customer who spent the most on orders:
SELECT c.customer_id, c.name, SUM(o.total_amount) AS Total_Spent
FROM orders o
JOIN customers c ON o.customer_id = c.customer_id
GROUP BY c.customer_id, c.name
ORDER BY Total_Spent DESC
LIMIT 1;

---

## 🧪 How to Run the Project
- Install PostgreSQL on your system.
- Open your SQL client (pgAdmin, DBeaver, or SQL Shell).
- Copy and execute the SQL script in the provided order:
- Create tables
- Insert sample data (if any)
- Run the queries
- Analyze the results and modify queries to explore more!

---

✨ Features
- Clean database design with normalization
- Beginner-friendly queries and logic
- Use of JOIN, GROUP BY, HAVING, ORDER BY, LIMIT, DISTINCT, etc.
- Revenue & inventory calculations
- Customer purchase analysis
  
---
