# 📊 MS EXCEL NOTES 

---

# 📅 WEEK 6 – DATA MANAGEMENT & CLEANING

---

## 🔹 1. Removing Duplicates

**Theory:**
Removes repeated rows from data

**Steps:**

* Select data → Data tab → Remove Duplicates

**Example:**
Data: A, B, A → Result: **A, B**

---

## 🔹 2. Text to Columns

**Theory:**
Splits one column into multiple columns

**Example:**
"Aditya,20" → becomes:
Name = Aditya | Age = 20

---

## 🔹 3. Data Validation

**Theory:**
Restricts input (like dropdowns)

**Example:**
Allow only: "Yes", "No"
👉 Prevents wrong data entry

---

## 🔹 4. Flash Fill

**Theory:**
Automatically detects pattern and fills data

**Example:**
Aditya Agarwal → you type “Aditya” once → Excel fills rest

---

# 🧠 FORMULA MASTERY

---

## 🔹 5. SUM

```excel
=SUM(A1:A5)
```

Adds numbers

---

## 🔹 6. COUNT

```excel
=COUNT(A1:A5)
```

Counts numbers only

---

## 🔹 7. AVERAGE

```excel
=AVERAGE(A1:A5)
```

---

## 🔹 8. SUMIFS

**Theory:**
Sum with conditions

```excel
=SUMIFS(B1:B10, A1:A10, "Aditya")
```

👉 Sum values where name = Aditya

---

## 🔹 9. COUNTIFS / AVERAGEIFS

Same concept with conditions

---

## 🔹 10. VLOOKUP

**Theory:**
Search vertically

```excel
=VLOOKUP(101, A1:C10, 2, FALSE)
```

👉 Finds ID 101 and returns column 2 value

---

## 🔹 11. HLOOKUP

Same as VLOOKUP but horizontal

---

## 🔹 12. XLOOKUP (MODERN 🔥)

```excel
=XLOOKUP(101, A1:A10, B1:B10)
```

👉 Better than VLOOKUP (more flexible)

---

## 🔹 13. INDEX

```excel
=INDEX(A1:C10, 2, 3)
```

👉 Value at row 2, column 3

---

## 🔹 14. MATCH

```excel
=MATCH(101, A1:A10, 0)
```

👉 Finds position

---

## 🔹 15. INDEX + MATCH 🔥

```excel
=INDEX(B1:B10, MATCH(101, A1:A10, 0))
```

👉 Powerful lookup combo

---

## 🔹 16. IF

```excel
=IF(A1>50, "Pass", "Fail")
```

---

## 🔹 17. IFERROR

```excel
=IFERROR(A1/B1, "Error")
```

---

## 🔹 18. AND / OR / NOT

```excel
=AND(A1>50, B1<100)
```

---

## 🔹 19. Nested Functions

**Theory:**
Functions inside functions

```excel
=IF(A1>50, IF(A1>80, "Top", "Pass"), "Fail")
```

---

## 🔹 20. ARRAY FORMULAS

**Theory:**
Work on multiple values at once

👉 Used in advanced calculations

---

## 🔹 21. LET

**Theory:**
Assign variable to simplify formulas

```excel
=LET(x, A1+A2, x*2)
```

---

## 🔹 22. SUMPRODUCT

```excel
=SUMPRODUCT(A1:A5, B1:B5)
```

👉 Multiply + sum

---

## 🔹 23. INDIRECT

```excel
=INDIRECT("A1")
```

👉 Refers to cell using text

---

## 🔹 24. CHOOSE

```excel
=CHOOSE(2, "A", "B", "C")
```

👉 Output = B

---

## 🔹 25. OFFSET

```excel
=OFFSET(A1, 1, 1)
```

👉 Moves from A1 → returns B2

---

## 🔹 26. LEFT / RIGHT

```excel
=LEFT(A1, 3)
=RIGHT(A1, 2)
```

👉 Extract text

---

# 📊 DATA ANALYSIS & REPORTING

---

## 🔹 27. Pivot Tables 🔥 (MOST IMPORTANT)

**Theory:**
Summarize data easily

👉 Convert raw data → insights

**Example:**
Sales data → total sales by city

---

## 🔹 28. Pivot Charts

Visual charts from pivot tables

---

## 🔹 29. Sorting & Filtering

**Sorting:** A-Z, High-Low
**Filtering:** Show specific data only

---

## 🔹 30. Subtotals

Adds grouped totals automatically

---

## 🔹 31. Data Tables

Used for scenario analysis

---

## 🔹 32. What-If Analysis

Test different inputs

---

## 🔹 33. Goal Seek

**Theory:**
Find input for desired output

👉 “What sales needed to reach ₹1,00,000 profit?”

---

## 🔹 34. Solver

**Theory:**
Optimization tool

👉 Max profit, minimize cost

---

# 📅 WEEK 7 – VISUALIZATION

---

## 🔹 35. Conditional Formatting

**Theory:**
Highlight data based on rules

👉 Example:
Red if < 50, Green if > 80

---

## 🔹 36. Charts

**Types:**

* Bar chart
* Line chart
* Pie chart

👉 Used for storytelling

---

## 🔹 37. Dynamic Dashboards 🔥

**Theory:**
Interactive reports using:

* Charts
* Pivot tables
* Slicers

👉 Used in real jobs

---

# ⚡ EFFICIENCY ENHANCERS

---

## 🔹 38. Keyboard Shortcuts

**Important ones:**

* Ctrl + C / V → Copy/Paste
* Ctrl + Z → Undo
* Ctrl + Arrow → Jump data
* Ctrl + Shift + L → Filter
* Alt + = → Auto SUM

---

## 🔹 39. Data Consolidation

Combine data from multiple sheets

---

## 🔹 40. Error Checking

Find & fix errors

👉 Example: #DIV/0!, #N/A

---

# 🚀 ADVANCED EXCEL

---

## 🔹 41. Advanced Filter

More powerful filtering

---

## 🔹 42. Slicers

Buttons to filter pivot tables

---

## 🔹 43. Timelines

Filter data by date

---
