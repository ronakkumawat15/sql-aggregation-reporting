# sql-aggregation-reporting
# SQL Project: Data Aggregation & Reporting

##  Description

This project demonstrates advanced SQL techniques for data aggregation and reporting using a real-world employee database. It focuses on generating business insights through grouping, filtering, and analytical queries.

---

##  Objective

To analyze employee and salary data and create meaningful reports using SQL aggregation functions and joins.

---

##  Tools Used

* MySQL
* SQL

---

##  Dataset

This project uses the **Employees Sample Database**:

* `employees` (300k+ records)
* `salaries` (2.8M+ records)
* `departments`
* `dept_emp`

---

##  Key Concepts Covered

* GROUP BY aggregation
* HAVING clause filtering
* Multi-table JOINs
* Window functions (LAG, SUM OVER)
* Data formatting (ROUND, FORMAT)
* Salary bucketization

---

## Project Structure

```
sql-aggregation-reporting/
│
├── README.md
├── queries/
│   ├── department_salary_summary.sql
│   ├── yearly_hiring_trends.sql
│   ├── high_earning_departments.sql
│   ├── salary_distribution.sql
│   ├── validation.sql
│
├── documentation/
│   └── explanation.md
│
└── outputs/
    ├── report1.png
    ├── report2.png
```

---

##  Reports Generated

### 1. Department Salary Summary

* Average, minimum, maximum salaries
* Employee count per department
* Salary range calculation

### 2. Yearly Hiring Trends

* Number of hires per year
* Year-over-year growth using window functions

### 3. High-Earning Departments

* Departments with high average salaries
* Filtered using HAVING clause

### 4. Salary Distribution Report

* Salary grouped into buckets
* Percentage distribution within departments

---

##  Sample Query

```sql
SELECT d.dept_name, ROUND(AVG(s.salary)) AS avg_salary
FROM departments d
JOIN dept_emp de ON d.dept_no = de.dept_no
JOIN salaries s ON de.emp_no = s.emp_no
GROUP BY d.dept_name
HAVING AVG(s.salary) > 70000;
```

---

##  Validation Checks

* Verified total current employees using COUNT(DISTINCT)
* Checked for NULL department values
* Ensured report totals match source data

---

## 📈 Skills Gained

* Writing analytical SQL queries
* Working with large datasets
* Data aggregation & reporting
* Query optimization basics

---

##  Key Learnings

* WHERE filters rows, HAVING filters groups
* COUNT(*) ensures data reliability
* Window functions enable trend analysis
* Proper joins are critical for accurate results

---

## Common Mistakes Avoided

* Misusing WHERE instead of HAVING
* Missing GROUP BY columns
* Division by zero errors
* Ignoring NULL values

---

##  Conclusion

This project demonstrates practical SQL skills used in data analysis, reporting, and business intelligence. It builds a strong foundation for advanced SQL and analytics roles.
