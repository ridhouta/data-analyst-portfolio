# Mental Health of International Students

## Business Question
Does length of stay affect mental health outcomes for international students?

## Dataset
Survey data from a Japanese international university (2018), approved by ethical review boards.
Students assessed on depression (PHQ-9), social connectedness (SCS), and acculturative stress (ASISS).

## SQL Query
```sql
SELECT stay, COUNT(*) AS count_int, 
       ROUND(AVG(todep),2) AS average_phq, 
       ROUND(AVG(tosc),2) AS average_scs, 
       ROUND(AVG(toas),2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC
LIMIT 9;
```

## Key Finding
International students with shorter length of stay tend to show higher acculturative stress 
and lower social connectedness — consistent with the study's published conclusions.

## Tools
PostgreSQL · DataCamp workspace
