

## SQL Queries Included

### 1. avg_exam_score_by_study_and_extracurricular
**Functions / Clauses Used:**  
- `SELECT`, `AVG()`, `WHERE`, `GROUP BY`, `ORDER BY`  

```sql
-- Calculate average exam score for students who study more than 10 hours and do extracurricular activities
SELECT hours_studied, AVG(exam_score) AS avg_exam_score
FROM student_performance
WHERE hours_studied > 10 
  AND extracurricular_activities = 'Yes'
GROUP BY hours_studied
ORDER BY hours_studied DESC;
