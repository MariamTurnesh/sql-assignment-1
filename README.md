# 🛒 SQL Retail Database Analysis

> Analysing a retail store database using SQL — exploring customer purchases, product sales and inventory data.

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-025E8C?style=for-the-badge&logo=amazondynamodb&logoColor=white)

---

## 📁 Project Structure

| File | Description |
|---|---|
| `schema.sql` | Creates the schema, tables and inserts all data |
| `queries.sql` | All 50 query solutions organised by topic |

---

## 🗄️ Database Structure

The **assignment** schema contains 4 tables:

| Table | Description |
|---|---|
| `customers` | 50 customers with membership tiers (Bronze, Silver, Gold) |
| `products` | 15 products across Electronics, Appliances and Accessories |
| `sales` | 15 sales transactions linking customers and products |
| `inventory` | Stock levels for each product |

### Relationships

```
customers ──── customer_id ────► sales ◄──── product_id ──── products
                                                │
                                           product_id
                                                │
                                           inventory
```

---

## 📋 Topics Covered

### 🔹 Basic SELECT
- Selecting all data, specific columns and filtered rows
- Using `WHERE` with operators — `>`, `<`, `=`, `BETWEEN`, `IN`, `LIKE`
- **`DISTINCT`** to remove duplicate values
- **`CONCAT`** to combine first and last name columns

### 🔹 Aggregate Functions
- **`COUNT`**, **`SUM`**, **`AVG`**, **`MIN`**, **`MAX`**
- Using **`AS`** aliases for clean, readable column names

### 🔹 GROUP BY & HAVING
- Grouping results by one or more columns
- Filtering grouped results with **`HAVING`**
- Key difference: `WHERE` filters rows, `HAVING` filters groups

### 🔹 Joins
- **`INNER JOIN`** across 2 and 3 tables
- **`LEFT JOIN`** to find unmatched records
- **Self Join** to compare rows within the same table
- Table aliases (`c`, `s`, `p`) for cleaner, shorter queries

### 🔹 Subqueries & UNION
- Subqueries inside `WHERE` to filter by aggregated values
- **`UNION`** to combine results from two separate queries into one result set

### 🔹 Date Functions
- Filtering by date range using **`BETWEEN`**
- Extracting year and month using **`EXTRACT`**
- Formatting dates using **`TO_CHAR`**
- Comparing dates by subtraction to find date differences

### 🔹 Sorting & Limiting
- **`ORDER BY`** with `ASC` and `DESC`
- **`LIMIT`** to return top N results

---

## 🧠 Key Concepts

```sql
-- The clause order every query follows
SELECT      -- what columns to show
FROM        -- which table
JOIN        -- connect other tables
WHERE       -- filter rows
GROUP BY    -- group results
HAVING      -- filter groups
ORDER BY    -- sort results
LIMIT       -- cap the results
```

> **The "for each / per / by" rule** — whenever a question uses these phrases, `GROUP BY` is needed.

> **WHERE vs HAVING** — `WHERE` filters *before* grouping, `HAVING` filters *after* grouping.

> **COUNT(DISTINCT)** — always use when counting unique entities after a JOIN to avoid duplicates.

---

## 🛠️ Tools Used

- **PostgreSQL** — database engine
- **pgAdmin** — SQL client
