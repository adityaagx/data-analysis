# 🗄️ SQL NOTES

---

## 🔹 1. CREATE

**Theory:**
Used to create a new table.

**Example:**

```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50),
    age INT
);
```

---

## 🔹 2. INSERT

**Theory:**
Adds new data into a table.

**Example:**

```sql
INSERT INTO students (id, name, age)
VALUES (1, 'Aditya', 20);
```

---

## 🔹 3. UPDATE

**Theory:**
Modifies existing data.

**Example:**

```sql
UPDATE students
SET age = 21
WHERE id = 1;
```

---

## 🔹 4. ALTER

**Theory:**
Changes table structure (add/remove column)

**Example:**

```sql
ALTER TABLE students
ADD email VARCHAR(100);
```

---

## 🔹 5. DELETE

**Theory:**
Removes specific rows

**Example:**

```sql
DELETE FROM students
WHERE id = 1;
```

---

## 🔹 6. DROP

**Theory:**
Deletes entire table permanently

**Example:**

```sql
DROP TABLE students;
```

---

## 🔹 7. TRUNCATE

**Theory:**
Deletes all data but keeps table structure

**Example:**

```sql
TRUNCATE TABLE students;
```

---

## 🔹 8. DATA TYPES

**Theory:**
Defines type of data stored in columns

**Common Types:**

* INT → numbers
* VARCHAR → text
* DATE → date
* FLOAT → decimal

**Example:**

```sql
age INT,
name VARCHAR(50)
```

---

# 🔍 QUERYING DATA

---

## 🔹 9. SELECT

**Theory:**
Fetch data from table

**Example:**

```sql
SELECT * FROM students;
```

---

## 🔹 10. DISTINCT

**Theory:**
Removes duplicate values

**Example:**

```sql
SELECT DISTINCT age FROM students;
```

---

## 🔹 11. WHERE

**Theory:**
Filters data

**Example:**

```sql
SELECT * FROM students
WHERE age > 18;
```

---

## 🔹 12. LIKE

**Theory:**
Pattern matching

**Example:**

```sql
SELECT * FROM students
WHERE name LIKE 'A%';
```

👉 Names starting with A

---

## 🔹 13. ORDER BY

**Theory:**
Sorts data

**Example:**

```sql
SELECT * FROM students
ORDER BY age DESC;
```

---

## 🔹 14. LIMIT / TOP

**Theory:**
Limits number of rows

**Example:**

```sql
SELECT * FROM students
LIMIT 5;
```

(SQL Server uses `TOP 5`)

---

## 🔹 15. AND / OR / NOT

**Theory:**
Logical conditions

**Example:**

```sql
SELECT * FROM students
WHERE age > 18 AND name = 'Aditya';
```

---

## 🔹 16. IN

**Theory:**
Matches multiple values

**Example:**

```sql
SELECT * FROM students
WHERE age IN (18, 20, 22);
```

---

## 🔹 17. BETWEEN

**Theory:**
Range filter

**Example:**

```sql
SELECT * FROM students
WHERE age BETWEEN 18 AND 25;
```

---

# 📅 WEEK 3 – AGGREGATION

---

## 🔹 18. SUM

```sql
SELECT SUM(age) FROM students;
```

---

## 🔹 19. MAX / MIN

```sql
SELECT MAX(age), MIN(age) FROM students;
```

---

## 🔹 20. COUNT

```sql
SELECT COUNT(*) FROM students;
```

---

## 🔹 21. AVG

```sql
SELECT AVG(age) FROM students;
```

---

## 🔹 22. GROUP BY

**Theory:**
Groups data

**Example:**

```sql
SELECT age, COUNT(*)
FROM students
GROUP BY age;
```

---

## 🔹 23. HAVING

**Theory:**
Filters grouped data

**Example:**

```sql
SELECT age, COUNT(*)
FROM students
GROUP BY age
HAVING COUNT(*) > 2;
```

---

# 🔗 JOINS (VERY IMPORTANT)

---

## 🔹 24. INNER JOIN

**Theory:**
Only matching data

```sql
SELECT *
FROM orders
INNER JOIN customers
ON orders.customer_id = customers.id;
```

---

## 🔹 25. LEFT JOIN

**Theory:**
All from left + matched from right

---

## 🔹 26. RIGHT JOIN

**Theory:**
All from right + matched from left

---

## 🔹 27. FULL OUTER JOIN

**Theory:**
All data from both tables

---

## 🔹 28. SELF JOIN

**Theory:**
Table joins with itself

```sql
SELECT a.name, b.name
FROM employees a
JOIN employees b
ON a.manager_id = b.id;
```

---

# 📅 WEEK 4 – ADVANCED

---

## 🔹 29. EXISTS

**Theory:**
Checks if subquery returns data

```sql
SELECT name
FROM customers c
WHERE EXISTS (
    SELECT 1 FROM orders o
    WHERE o.customer_id = c.id
);
```

---

## 🔹 30. UNION

**Theory:**
Combines results (removes duplicates)

```sql
SELECT name FROM students
UNION
SELECT name FROM teachers;
```

---

## 🔹 31. UNION ALL

**Theory:**
Includes duplicates

---

## 🔹 32. DATE FUNCTIONS

**Examples:**

```sql
SELECT NOW();
SELECT YEAR(NOW());
```

---

## 🔹 33. CTE (Common Table Expression)

**Theory:**
Temporary result set

```sql
WITH temp AS (
    SELECT * FROM students WHERE age > 18
)
SELECT * FROM temp;
```

---

## 🔹 34. SUBQUERY

**Theory:**
Query inside another query

```sql
SELECT *
FROM students
WHERE age > (SELECT AVG(age) FROM students);
```

---

# 🔹 35. CASE WHEN

**Theory:**
Conditional logic

```sql
SELECT name,
CASE 
    WHEN age > 18 THEN 'Adult'
    ELSE 'Minor'
END
FROM students;
```

---

# 🔹 36. WINDOW FUNCTIONS 🔥 (VERY IMPORTANT)

---

## 🔹 ROW_NUMBER()

```sql
SELECT name,
ROW_NUMBER() OVER (ORDER BY age) AS rn
FROM students;
```

---

## 🔹 RANK()

Same rank → gaps exist

---

## 🔹 DENSE_RANK()

No gaps in ranking

---

## 🔹 LEAD / LAG

Access next/previous row

```sql
SELECT name,
LAG(age) OVER (ORDER BY age)
FROM students;
```

---

## 🔹 NTILE()

Divides data into groups

---

## 🔹 FIRST_VALUE / LAST_VALUE

Get first/last value in window

---

# 🔹 37. AGGREGATE AS WINDOW FUNCTION

**Theory:**
Apply aggregate without grouping rows

```sql
SELECT name,
AVG(age) OVER () AS avg_age
FROM students;
```

---
