SELECT Name, Grade, Marks
FROM (
    SELECT
        CASE
            WHEN Marks >= 70 THEN Name
            ELSE NULL
        END AS Name,
        CASE 
            WHEN Marks < 100 THEN (FLOOR(Marks / 10) + 1)
            WHEN MARKS = 100 THEN 10
        END AS Grade,
        Marks
    FROM Students
) AS SUBQUERY
ORDER BY Grade DESC, NAME ASC;
    
