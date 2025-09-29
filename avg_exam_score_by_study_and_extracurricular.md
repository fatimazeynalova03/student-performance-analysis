

## SQL Queries Included

### 1. avg_exam_score_by_study_and_extracurricular
**Functions / Clauses Used:**  
- `SELECT` → Chooses which columns to display.
- `AVG()` → Calculates the average value of a numeric column.
- `WHERE` → Filters rows that meet certain conditions.
- `GROUP BY` → Groups rows so aggregate functions can be applied to each group.
- `ORDER BY` → Sorts the results by one or more columns.

```sql
-- Calculate average exam score for students who study more than 10 hours and do extracurricular activities
SELECT hours_studied, AVG(exam_score) AS avg_exam_score
FROM student_performance
WHERE hours_studied > 10 
  AND extracurricular_activities = 'Yes'
GROUP BY hours_studied
ORDER BY hours_studied DESC;
