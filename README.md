# 🎵 SQL Music Store Analysis using PostgreSQL

> A SQL portfolio project that analyzes a music store database using **PostgreSQL** to answer real-world business questions related to customers, sales, artists, genres, and revenue.

---

# 📌 Project Overview

This project explores the **Chinook Music Store Database** using **PostgreSQL**. The objective is to solve business-oriented analytical problems by writing SQL queries ranging from basic aggregations to advanced Common Table Expressions (CTEs) and Window Functions.

The project demonstrates practical SQL skills commonly used in Data Analyst and Business Intelligence roles.

---

# 🛠 Tech Stack

* **Database:** PostgreSQL
* **Language:** SQL
* **Tool:** pgAdmin (or PostgreSQL-compatible SQL Editor)
* **Version Control:** Git & GitHub

---

# 📂 Database Schema

The project uses the Chinook Music Store relational database.

> **Insert your schema diagram below**

<p align="center">
![Database Schema](<img width="710" height="574" alt="MusicDatabaseSchema" src="https://github.com/user-attachments/assets/fd12f051-f2cb-49ef-8c2b-70ea62cdb52c" />)

![Database Schema](images/database_schema.png)

</p>

---

# 🗄 Database Tables

| Table         | Description              |
| ------------- | ------------------------ |
| Employee      | Employee information     |
| Customer      | Customer details         |
| Invoice       | Customer invoices        |
| InvoiceLine   | Purchased tracks         |
| Track         | Song information         |
| Album         | Album details            |
| Artist        | Artist information       |
| Genre         | Music genres             |
| Playlist      | Playlist information     |
| PlaylistTrack | Playlist-track mapping   |
| MediaType     | Audio format information |

---

# 🧠 SQL Concepts Used

* SELECT
* WHERE
* ORDER BY
* GROUP BY
* COUNT()
* SUM()
* AVG()
* INNER JOIN
* Subqueries
* Common Table Expressions (CTEs)
* Window Functions
* ROW_NUMBER()
* LIMIT

---

# 📈 Business Questions Solved

## 🟢 Easy Level

### 1. Who is the senior-most employee based on job title?

**Objective**

Find the employee with the highest job level.

**SQL Query**

> *(Insert screenshot below)*

![Query 1](images/query1.png)

---

### 2. Which countries have the most invoices?

**Objective**

Identify countries generating the highest number of invoices.

![Query 2](images/query2.png)

---

### 3. What are the top 3 invoice totals?

**Objective**

Retrieve the highest invoice amounts.

![Query 3](images/query3.png)

---

### 4. Which city generated the highest revenue?

**Objective**

Determine the city with the highest total sales.

![Query 4](images/query4.png)

---

### 5. Who is the best customer?

**Objective**

Identify the customer who spent the most money.

![Query 5](images/query5.png)

---

# 🟡 Moderate Level

### 6. Rock Music Listeners

**Objective**

Retrieve customers who purchased Rock music.

![Query 6](images/query6.png)

---

### 7. Top 10 Rock Artists

**Objective**

Find artists with the highest number of Rock tracks.

![Query 7](images/query7.png)

---

### 8. Tracks Longer Than Average

**Objective**

List songs longer than the average track duration.

![Query 8](images/query8.png)

---

# 🔴 Advanced Level

### 9. Customer Spending by Artist

**Objective**

Calculate how much each customer spent on the best-selling artist.

![Query 9](images/query9.png)

---

### 10. Most Popular Genre by Country

**Objective**

Identify the most purchased music genre in every country.

![Query 10](images/query10.png)

---

### 11. Top Customer by Country

**Objective**

Determine the highest spending customer in each country.

![Query 11](images/query11.png)

---

# 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Writing complex SQL queries
* Working with relational databases
* Performing multi-table joins
* Using aggregate functions
* Implementing subqueries
* Building Common Table Expressions (CTEs)
* Applying Window Functions
* Solving business-oriented SQL problems
* Analyzing customer purchasing behavior
* Generating actionable business insights

---

# 📁 Project Structure

```text
SQL-Music-Store-Analysis/
│
├── README.md
├── Music_Store_Analysis.sql
├── Dataset/
│
├── images/
│   ├── database_schema.png
│   ├── query1.png
│   ├── query2.png
│   ├── query3.png
│   ├── query4.png
│   ├── query5.png
│   ├── query6.png
│   ├── query7.png
│   ├── query8.png
│   ├── query9.png
│   ├── query10.png
│   └── query11.png
│
└── presentation/
    └── SQL_Music_Store_Analysis.pptx
```

---

# 🚀 Future Improvements

* Add interactive Power BI dashboard
* Build Tableau visualizations
* Write additional business-focused SQL queries
* Optimize query performance
* Perform exploratory data analysis using Python

---

# 📬 Connect With Me

**GitHub:** https://github.com/yourusername

**LinkedIn:** https://linkedin.com/in/yourprofile

**Email:** [your.email@example.com](mailto:your.email@example.com)

---

⭐ If you found this project useful, consider giving the repository a **Star**.
