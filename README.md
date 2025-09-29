# Student Performance Analysis

## Project Description
This project explores how study habits and extracurricular activities influence student exam performance. Using SQL queries on the `student_performance` dataset, we uncover insights that can help students, teachers, and policymakers improve learning outcomes.

The dataset contains details about attendance, study hours, sleep, tutoring sessions, teacher quality, extracurricular participation, and exam scores.

---

## Dataset: `student_performance`

| Column | Definition | Data Type |
|--------|------------|-----------|
| attendance | Percentage of classes attended | float |
| extracurricular_activities | Participation in extracurricular activities | varchar (Yes, No) |
| sleep_hours | Average number of hours of sleep per night | float |
| tutoring_sessions | Number of tutoring sessions attended per month | integer |
| teacher_quality | Quality of the teachers | varchar (Low, Medium, High) |
| exam_score | Final exam score | float |
| hours_studied | Number of study hours per week | float |
### 1. `avg_exam_score_by_study_and_extracurricular.sql`
**Purpose:** Calculate the average exam score for students who study more than 10 hours per week and participate in extracurricular activities.  
**Functions / Clauses Used:** `SELECT`, `AVG()`, `WHERE`, `GROUP BY`, `ORDER BY`  
### 2.  `avg_exam_score_by_hours_studied_range.sql`
**Purpose:** Group students into study hour ranges and calculate the average exam score for each range.
**Functions / Clauses Used:** `SELECT`, `CASE WHEN`, `AVG()`, `ROUND()`, `GROUP BY`, `ORDER BY`
### 3.  `student_exam_ranking.sql`
**Purpose:** Rank students based on their exam scores using `DENSE_RANK()` and return the top 30 students.
**Functions / Clauses Used:** SELECT, `DENSE_RANK()`, `OVER(...)`, `ORDER BY`, `LIMIT`
