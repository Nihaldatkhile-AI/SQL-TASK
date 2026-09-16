# ♻️ E-Waste Collection and Recycling Network – SQL Project

## 📌 Project Overview

The **E-Waste Collection and Recycling Network** is a MySQL database project created to manage and analyze electronic waste collection activities.

The system stores information about **donors, collection centres, electronic device categories, recycling partners, and e-waste collections**.

The project focuses on using SQL to retrieve, filter, organize, and analyze data while solving practical business-related questions.

---

## 🗄️ Database Information

**Database Name:** `ewaste_network`
**Database:** MySQL 8.x
**Collection Records:** 200

### Main Tables

| Table                | Description                                 |
| -------------------- | ------------------------------------------- |
| `donors`             | Stores donor information                    |
| `collection_centers` | Stores collection centre details            |
| `device_categories`  | Stores different e-waste device categories  |
| `recycling_partners` | Stores authorized recycling partner details |
| `collections`        | Stores e-waste collection records           |

### Database Relationship

```text
                    E-WASTE DATABASE
                          │
                          ▼
                     Collections
                    /     |      \
                   /      |       \
                  ▼       ▼        ▼
              Donors   Centers   Devices
                          │
                          ▼
                  Recycling Partners
```

The `collections` table connects the main entities using **foreign keys**.

---

# 📊 Project Data

The database contains information such as:

* Donor name and type
* Donor city and contact details
* Collection centre location and capacity
* Electronic device category
* Hazard level
* Recyclable percentage
* Collection date
* Collection channel
* Quantity and weight
* Condition grade
* Recovered value
* CO₂ savings
* Recycling status
* Recycling partner information

---

# 🛠️ SQL Concepts Used

This project covers both basic and advanced SQL concepts.

### Basic SQL

* `CREATE DATABASE`
* `CREATE TABLE`
* `INSERT`
* `SELECT`
* `WHERE`
* `DISTINCT`
* `ORDER BY`
* `LIMIT`

### Filtering & Conditions

* `AND`
* `OR`
* `NOT`
* `IN`
* `BETWEEN`
* `LIKE`
* `IS NULL`
* `IS NOT NULL`

### Data Analysis

* `COUNT()`
* `SUM()`
* `AVG()`
* `MIN()`
* `MAX()`
* `GROUP BY`
* `HAVING`

### Advanced SQL

* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`
* `UNION`
* Subqueries
* `CASE`
* Nested conditions
* Views
* Indexes

### Database Concepts

* Primary Keys
* Foreign Keys
* Constraints
* `CHECK`
* `UNIQUE`
* `ENUM`
* Relationships
* Indexing

---

# 📈 Business Analysis Questions

## 1. Donor Analysis

1. Display all registered donors.
2. Display unique donor cities.
3. Find donors based on donor type.
4. Find donors from a particular city.
5. Find donors whose names start with `A`.
6. Find donors whose names contain the letter `a`.
7. Identify donors with missing contact information.
8. Count donors by donor type.
9. Count donors in each city.
10. Find donors who have made more than 5 collections.
11. Find the donor with the highest total e-waste contribution.

---

## 2. Collection Centre Analysis

1. Display all collection centres.
2. Find active collection centres.
3. Find centres with capacity greater than 3,000 kg.
4. Display centres ordered by capacity.
5. Find the centre with the highest capacity.
6. Count collection centres by city.
7. Calculate total e-waste collected by each centre.
8. Find centres handling more than a specified number of collections.
9. Compare collected weight with centre capacity.

---

## 3. Device Category Analysis

1. Display all device categories.
2. Find devices with recyclable percentage above 80%.
3. Find devices with `High` or `Critical` hazard levels.
4. Find devices with average weight above a specified value.
5. Find the category with the highest recyclable percentage.
6. Find the category with the highest base rate.
7. Calculate total collected weight by device category.
8. Calculate total recovered value by device category.
9. Calculate total CO₂ savings by device category.

---

## 4. Collection Analysis

1. Display all collection records.
2. Find collections above 50 kg.
3. Find collections with recovered value above ₹5,000.
4. Find collections with CO₂ savings above 100 kg.
5. Display the top 10 collections by recovered value.
6. Display collections from a particular channel.
7. Count collections by status.
8. Count collections by collection channel.
9. Calculate total collection weight.
10. Calculate average collection weight.
11. Calculate total recovered value.
12. Calculate total CO₂ savings.
13. Find the highest and lowest collection weight.

---

## 5. Recycling Partner Analysis

1. Display all recycling partners.
2. Display partners along with their certification details.
3. Count collections handled by each partner.
4. Calculate total weight handled by each partner.
5. Calculate total recovered value associated with each partner.
6. Find the partner with the highest collection weight.
7. Find the partner with the highest recovered value.

---

# 🔗 JOIN Analysis

Use SQL JOINs to combine information from multiple tables.

### Questions

1. Display collection ID along with donor name and collection date.
2. Display collection centre name along with collection weight.
3. Display device category along with collected weight.
4. Display recycling partner along with collection status.
5. Display donor name, device category, weight, and recovered value.
6. Display collection centre, device category, and recycling partner.
7. Create a combined result containing:

```text
Collection ID
Donor Name
Collection Centre
Device Category
Recycling Partner
Collection Date
Weight
Recovered Value
CO₂ Saved
Status
```

8. Display all donors including donors who have not made any collections.

---

# 🧠 Advanced SQL Analysis

### Subqueries

1. Find collections having weight greater than the average collection weight.
2. Find collections having recovered value greater than the average.
3. Find device categories having recyclable percentage above the average.
4. Find collection centres having capacity above the average capacity.

### CASE Statements

Classify collection weight:

```text
Low       → Below 10 kg
Medium    → 10–30 kg
High      → Above 30 kg
```

Classify recovered value:

```text
Low       → Below ₹1,000
Medium    → ₹1,000–₹5,000
High      → Above ₹5,000
```

Use `CASE + GROUP BY` to count records in each category.

---

# 👁️ SQL View

A reusable SQL view named `v_collection_full` is included in the project.

The view combines information from the collection, donor, collection centre, device category, and recycling partner tables.

Example:

```sql
SELECT *
FROM v_collection_full;
```

This demonstrates how a **SQL VIEW** can simplify repeated multi-table analysis.

---

# ⚡ Indexing

Indexes are created on commonly searched columns in the `collections` table, such as:

```text
collection_date
status
center_id
category_id
```

Indexes demonstrate how SQL databases can improve query performance when working with frequently searched or filtered data.

---

# 📂 Project Files

```text
E-Waste-SQL-Project/
│
├── 01_schema_and_data.sql
└── README.md
```

### `01_schema_and_data.sql`

Contains:

* Database creation
* Table creation
* Data insertion
* Primary keys
* Foreign keys
* Constraints
* Indexes
* SQL View
* Collection records

---

# ▶️ How to Run

1. Open **MySQL Workbench**.
2. Open `01_schema_and_data.sql`.
3. Execute the complete SQL script.
4. Select the database:

```sql
USE ewaste_network;
```

5. Verify the collection data:

```sql
SELECT COUNT(*)
FROM collections;
```

The project contains **200 collection records**.

---

# 🎓 Skills Demonstrated

Through this project, I practiced:

* Relational database design
* SQL data retrieval
* Data filtering and sorting
* Aggregate analysis
* GROUP BY and HAVING
* Multiple-table JOINs
* Subqueries
* CASE statements
* Views
* Indexes
* Primary and Foreign Keys
* Database constraints
* Business-oriented problem solving

---

# 🏁 Project Conclusion

This project demonstrates how SQL can be used to organize and analyze data for a real-world **e-waste collection and recycling network**.

By analyzing donors, collection centres, device categories, recycling partners, collection activity, recovered value, and environmental impact, the database can provide useful information for understanding the overall recycling process.

The project also provides practical experience with both **fundamental and advanced SQL concepts**.

---

# 🎯 Goal

The goal of this project is to **strengthen my practical SQL and database skills by working with a realistic business problem**.

I aim to improve my ability to **design databases, write SQL queries, analyze data, solve business questions, and build a strong foundation for my Data Analyst / Data Science career.**
