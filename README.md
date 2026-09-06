# ♻️ E-Waste Collection and Recycling Network

## Scenario

The **E-Waste Collection and Recycling Network** is a MySQL-based system designed to manage and analyze electronic waste collection and recycling activities.

The system stores information about **collection centres, device categories, recycling partners, donors, and e-waste collections**.

The project helps analyze the quantity of e-waste collected, recycling performance, recovered value, hazardous materials, and CO₂ emissions avoided.

---

# 1. Collection Centres

The network operates through multiple collection centres across cities such as **Mumbai, Thane, Dombivli, Pune, Nashik, Nagpur, Bengaluru, Hyderabad, Ahmedabad, Indore, and Jaipur**.

For each centre, the system stores:

* Centre name
* City and state
* Pincode
* Capacity in kg
* Opening date
* Active status

A collection centre can receive e-waste from many donors.

---

# 2. Device Categories

The system maintains different categories of electronic devices, such as:

* Smartphone
* Laptop
* Desktop CPU Cabinet
* CRT Monitor
* LED Television
* Printer
* Lithium Ion Battery Pack
* Wi-Fi Router and Modem
* Split Air Conditioner
* Washing Machine

For each category, the system stores its **hazard level, average weight, recyclable percentage, recycling rate, and CO₂ saving factor**.

---

# 3. Recycling Partners

The network works with authorized recycling companies.

For each partner, the system stores:

* Partner name
* Certification
* City
* Contract start date
* Rate multiplier

A recycling partner can process multiple e-waste collections.

---

# 4. Donors

Donors are individuals and organizations that hand over electronic waste to the network.

Donor types include:

* Household
* Office
* School
* Retail

The system stores donor name, type, city, state, email, and registration date.

---

# 5. Collections

The **Collections** table is the main transaction table of the project.

It contains **200 collection records**.

For every collection, the system records:

* Donor
* Collection centre
* Device category
* Recycling partner
* Collection date
* Collection channel
* Quantity
* Weight
* Condition grade
* Recovered value
* CO₂ saved
* Processing status

Collection channels include:

* Walk In
* Doorstep Pickup
* Bulk Drive
* Corporate Tie Up

Processing statuses include:

* Collected
* In Transit
* Dismantled
* Recycled
* Refurbished

---

# SQL

## E-Waste Collection & Recycling Network

```text
E-WASTE NETWORK
       │
       ▼
   SQL DATABASE
       │
       ├── Collection Centres
       ├── Device Categories
       ├── Recycling Partners
       ├── Donors
       └── Collections
       │
       ▼
   SQL ANALYSIS
       │
       ├── SELECT
       ├── WHERE
       ├── GROUP BY
       ├── HAVING
       ├── JOIN
       ├── SUBQUERY
       ├── CTE
       ├── WINDOW FUNCTIONS
       └── CASE
       │
       ▼
    INSIGHTS
       │
       ├── E-Waste Volume
       ├── Centre Performance
       ├── Donor Analysis
       ├── Partner Performance
       ├── CO₂ Savings
       └── Recycling Status
```

## SQL Analysis

The project contains **15 analysis queries**, covering:

* Overall e-waste collection performance
* Device category analysis
* Critical-hazard waste monitoring
* Collection centre performance
* Donor type analysis
* Monthly collection trends
* Condition grade analysis
* High-performing donors
* Donors with no collections
* Recycling partner scorecards
* Top 3 categories by city
* Cumulative CO₂ savings
* Collection channel analysis
* Refurbishment funnel
* Top 10 most valuable collections

## SQL Concepts Used

* `SELECT`
* `WHERE`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* `JOIN`
* `LEFT JOIN`
* Aggregate Functions
* Subqueries
* CTEs
* Window Functions
* `RANK()`
* `CASE WHEN`
* Date Functions
* Views
* Indexes
* Primary Keys
* Foreign Keys
* Constraints

## Database

**Database:** `ewaste_network`
**Engine:** MySQL 8.x
**Main Table:** `collections`
**Records:** 200

## Project Structure

```text
E-Waste-Collection-and-Recycling-Network/
│
├── 01_schema_and_data.sql
├── 02_analysis_queries.sql
└── README.md
```

## Tools Used

* MySQL 8.x
* MySQL Workbench
* SQL
* GitHub

## Project Goal

The goal of this project is to demonstrate how **SQL and relational databases can be used to manage e-waste operations and generate useful environmental and business insights**.

**E-Waste → SQL Database → Analysis → Insights → Sustainability ♻️**
