## SQL Queries Included
### 3. student_exam_ranking
**Functions / Clauses Used:**  
- `SELECT` → choose columns to display  
- `DENSE_RANK() OVER()` → assign ranks to students based on exam score  
- `ORDER BY` → sort ranks ascending  
- `LIMIT` → restrict output to top 30 students  

```sql
-- Rank students by exam score without revealing the scores to each other
SELECT 
    attendance, 
    hours_studied, 
    sleep_hours, 
    tutoring_sessions,
    DENSE_RANK() OVER(ORDER BY exam_score DESC) AS exam_rank
FROM student_performance
ORDER BY exam_rank ASC
LIMIT 30;
