###### 2. avg_exam_score_by_hours_studied_range
**Functions / Clauses Used:**  
- `SELECT` → choose columns to display  
- `CASE WHEN` → categorize students into study hour ranges  
- `AVG()` → calculate average exam score  
- `ROUND()` → round the average to 2 decimal places  
- `GROUP BY` → group results by study hour ranges  
- `ORDER BY` → sort results by average exam score descending  

```sql
-- Categorize students by hours studied and calculate average exam score for each range
SELECT
    CASE
        WHEN hours_studied BETWEEN 1 AND 5 THEN '1-5 hours'
        WHEN hours_studied BETWEEN 6 AND 10 THEN '6-10 hours'
        WHEN hours_studied BETWEEN 11 AND 15 THEN '11-15 hours'
        WHEN hours_studied >= 16 THEN '16+ hours'
    END AS hours_studied_range,
    ROUND(AVG(exam_score), 2) AS avg_exam_score
FROM student_performance
GROUP BY hours_studied_range
ORDER BY avg_exam_score DESC;
