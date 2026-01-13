# Gender-Pay-and-Role-Disparity-Analysis-Using-Employee-Records

## Introduction
This project analyzes employee records from an organization to investigate **gender-based disparities in pay and role distribution**. The dataset is structured and resembles data from a Human Resources Information System (HRIS), containing information on departments, divisions, gender, salary components, and job grades.

The core research question addressed in this project is:

**Are there any disparities in pay and roles based on gender within the organization?**

---

## Dataset-Overview
- **Source:** data.gov – Employee Salaries 2023  
- **Link:** https://catalog.data.gov/dataset/employee-salaries-2023

### Dataset-Attributes
- **Department** – Department name  
- **Division** – Division within the department  
- **Gender** – Employee gender (M/F)  
- **Base-Salary** – Base annual compensation  
- **Overtime-Pay** – Overtime compensation  
- **Longevity-Pay** – Pay based on employee tenure  
- **Grade** – Job level or rank  

---

## Use-Cases
- Gender pay gap analysis  
- Diversity and inclusion assessment  
- Human resource planning  
- Policy evaluation for fair compensation and promotions  

---

## Database-Design
The dataset is stored in a **PostgreSQL** relational database using a normalized schema:

- **department_table** – Stores department-level data  
- **division_table** – Stores division-level data  
- **employee_table** – Stores employee demographic and salary information  

An Entity Relationship (ER) diagram was created to visualize table relationships.

---

## Tools-and-Technologies
- **Database:** PostgreSQL  
- **Programming Language:** Python  
- **Libraries:** pandas, psycopg2, matplotlib  
- **Environment:** Jupyter Notebook  

---

## Data-Ingestion
- CSV data is imported into PostgreSQL using `psycopg2`
- Bulk inserts are handled using `COPY` and `copy_from()` methods
- Data is pre-processed into department, division, and employee tables

---

## Exploratory-Data-Analysis

### Gender-Distribution
A pie chart analysis shows that the overall number of male and female employees is relatively balanced at the organizational level.

### Salary-Comparison-by-Gender
- Mean and median base salaries were compared between genders  
- Bar plots show noticeable differences, but descriptive statistics alone are insufficient for definitive conclusions  

### Role-Distribution-by-Division
- Stacked bar charts reveal divisions with significant gender imbalance  
- Some divisions are dominated by a single gender, indicating potential inequality in role allocation  

### Division-Level-Pay-Disparities
- Analysis was limited to divisions with **at least 10 male and 10 female employees** to avoid skewed results  
- The top 20 divisions with the largest mean pay gaps were visualized  
- In most divisions, male employees earn higher average salaries, though exceptions exist  

---

## Key-Findings
- Overall gender representation is balanced, but division-level imbalances are present  
- Pay disparities exist across multiple divisions  
- The pay gap is not uniform and varies by division  
- Results suggest systemic issues rather than isolated cases  

---

## Conclusion
The analysis indicates meaningful **gender-based disparities in both pay and role allocation** within the organization. While overall gender counts appear balanced, division-level analysis reveals persistent inequalities in compensation and workforce composition.

These findings emphasize the need for:
- Reviewing compensation and promotion policies  
- Conducting deeper statistical testing  
- Implementing long-term diversity and pay equity monitoring  

---

