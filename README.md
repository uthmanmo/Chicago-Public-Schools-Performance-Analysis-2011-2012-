---

# Chicago Public Schools Performance Analysis (2011-2012)

## 🧠 Project Overview

This project analyzes the performance of Chicago Public Schools for the year 2011-2012 using real-world data. The analysis includes safety scores, student attendance rates, college enrollment, and hardship indexes by community area.

i used **Python**, **SQLite**, and **SQL queries** inside a **Jupyter Notebook** to load, transform, and analyze the data.

## 📦 Technologies Used

- Python
- SQLite3
- Pandas
- IPython-SQL
- PrettyTable
- Jupyter Notebook

---

## 📌 Objective

- Store real-world CSV data into a SQLite database.
- Query the data using SQL within a Jupyter Notebook.
- Explore school performance indicators.
- Retrieve table and column metadata.
- Use SQL functions for deeper analysis.
---

## 📂 Data Sources

- [Chicago Public Schools Data (CSV)](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/FinalModule_Coursera_V5/data/ChicagoPublicSchools.csv)
- [Chicago Census Data (CSV)](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/FinalModule_Coursera_V5/data/ChicagoCensusData.csv)

## 🔍 Key Analyses

- Displayed all tables in the database
- Calculated total number of schools
- Found schools with highest and lowest safety scores
- Identified top and bottom schools by attendance
- Cleaned attendance data to remove '%'
- Converted data to numeric types for comparison
- Aggregated college enrollment by community area
- Connected school data with census data to find hardship index for specific community areas

---

## Metrics include

- ISAT Scores
- Safety and Environment ratings
- Student Growth
- College Enrollment
- School Climate
- Student/Teacher Ratios
- And  more...

## 🧪 Sample SQL Queries Used

```sql
SELECT MAX(Safety_Score) AS MAX_SAFETY_SCORE FROM CHICAGO_PUBLIC_SCHOOLS_DATA;
SELECT Name_of_School, Average_Student_Attendance FROM CHICAGO_PUBLIC_SCHOOLS_DATA ORDER BY Average_Student_Attendance DESC LIMIT 10;
SELECT Community_Area_Name, SUM(College_Enrollment) AS TOTAL_ENROLLMENT FROM CHICAGO_PUBLIC_SCHOOLS_DATA GROUP BY Community_Area_Name;
