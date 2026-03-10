# Statistics & Math for Data Analysis

This document contains quick reference notes for fundamental **statistics and mathematics concepts used in data analysis**. These concepts help analysts summarize data, understand distributions, and perform calculations needed for decision-making.

---

# 1. Basic Statistics

## Mean (Average)

The **mean** is the average value of a dataset. It is calculated by adding all the values and dividing by the number of observations.

**Formula**

Mean = (Sum of all values) / (Number of values)

**Example**

Values: 10, 20, 30  
Mean = (10 + 20 + 30) / 3 = 20

**Use Cases**
- Average sales
- Average revenue per user
- Average customer spending

---

## Median

The **median** is the middle value of a dataset when the values are arranged in ascending order.

**Example (Odd number of values)**

Dataset: 2, 4, 6, 8, 10  
Median = 6

**Example (Even number of values)**

Dataset: 2, 4, 6, 8  
Median = (4 + 6) / 2 = 5

**Use Cases**
- Income analysis
- Datasets with extreme outliers

---

## Mode

The **mode** is the value that appears most frequently in a dataset.

**Example**

Dataset: 1, 2, 2, 3, 4  
Mode = 2

**Types**
- Unimodal → one mode
- Bimodal → two modes
- Multimodal → more than two modes

**Use Cases**
- Most popular product
- Most frequent category in a dataset

---

## Variance

**Variance** measures how far each data point is from the mean.

It indicates how spread out the data values are.

**Concept**

Variance = Average of squared differences from the mean.

**Use Cases**
- Measuring variability in datasets
- Financial risk analysis

---

## Standard Deviation (SD)

**Standard deviation** measures the average distance of each data point from the mean.

- Small SD → data points are close to the mean
- Large SD → data points are widely spread

**Relationship**

Standard Deviation = √Variance

**Use Cases**
- Stock market volatility
- Sales variability
- Risk measurement

---

## Measures of Dispersion

Measures of dispersion describe how spread out data values are.

**Common Measures**
- Range
- Variance
- Standard Deviation
- Quartiles
- Interquartile Range (IQR)

**Example**

Dataset A: 50, 50, 50, 50  
Dataset B: 10, 30, 70, 90  

Both datasets may have the same mean but very different spreads.

---

## Normal Distribution

A **normal distribution** is a probability distribution where data forms a symmetric bell-shaped curve.

**Characteristics**

- Mean = Median = Mode
- Symmetrical around the center
- Most data lies near the mean

**Empirical Rule**

- 68% of data lies within 1 standard deviation
- 95% lies within 2 standard deviations
- 99.7% lies within 3 standard deviations

**Use Cases**
- Exam scores
- Heights of people
- Measurement errors

---

## Percentiles

A **percentile** indicates the value below which a certain percentage of data falls.

**Examples**

50th percentile → Median  
90th percentile → 90% of data lies below this value

**Use Cases**
- Exam rankings
- Salary distribution
- Performance benchmarking

---

## Quartiles

**Quartiles** divide a dataset into four equal parts.

**Types**

Q1 → 25th percentile  
Q2 → 50th percentile (Median)  
Q3 → 75th percentile

**Interquartile Range (IQR)**

IQR = Q3 − Q1

**Use Cases**
- Detecting outliers
- Understanding data spread

---

## Probability

**Probability** measures the likelihood of an event occurring.

**Formula**

Probability = Favorable outcomes / Total possible outcomes

**Example**

Probability of getting heads in a coin toss = 1/2

**Probability Range**

0 → Impossible event  
1 → Certain event

**Use Cases**
- Predictive modeling
- Risk assessment
- Machine learning algorithms

---

# 2. Basic Math for Data Analysis

## Arithmetic

Arithmetic involves basic mathematical operations:

- Addition (+)
- Subtraction (-)
- Multiplication (×)
- Division (÷)

These operations are fundamental for performing calculations in data analysis.

**Use Cases**

- Calculating totals
- Data transformations
- Basic numerical analysis

---

## Weighted Average

A **weighted average** assigns different levels of importance (weights) to values.

**Formula**

Weighted Average = (Σ value × weight) / (Σ weights)

**Example**

Marks:

Math: 90 (weight 50%)  
Science: 80 (weight 30%)  
English: 70 (weight 20%)

Weighted average = (90×0.5 + 80×0.3 + 70×0.2)

**Use Cases**

- GPA calculation
- Portfolio returns
- Performance scoring systems

---

## Cumulative Sum

**Cumulative sum** is the running total of a sequence of numbers.

Each value is added to the previous total.

**Example**

Dataset: 5, 10, 15, 20

Cumulative Sum:

5  
5 + 10 = 15  
15 + 15 = 30  
30 + 20 = 50

Result: 5, 15, 30, 50

**Use Cases**

- Running revenue totals
- Time series analysis
- Tracking growth over time

---

# Summary

These statistics and mathematical concepts form the **foundation of data analysis**. They help analysts:

- Summarize large datasets
- Understand patterns and distributions
- Measure variability
- Perform calculations required for decision-making

Mastering these fundamentals is essential before moving to tools like **SQL, Python, Excel, and data visualization platforms**.
