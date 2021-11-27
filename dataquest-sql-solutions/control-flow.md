1. If... Then in SQL
```SQL
SELECT invoice_id, total, 
       (CASE 
        WHEN total>10 THEN 'High' 
        ELSE 'Low' END) AS total_category
  FROM invoice;
```

2. Multiple If... Thens
```SQL
SELECT invoice_id, total,
       (CASE
        WHEN total>10 THEN 'High'
        WHEN total>5 AND total<=10 THEN 'Medium'
        WHEN total<=5 THEN 'Low'
        ELSE 'Unknown' END) AS total_category
  FROM invoice;
```

3. Or ELSE...
```SQL
SELECT first_name, last_name, title, reports_to,
       (CASE
         WHEN reports_to = 1 THEN 'Adams'
         WHEN reports_to = 2 THEN 'Edwards'
         WHEN reports_to = 6 THEN 'Mitchell'
         WHEN reports_to IS NULL THEN 'Self'
        END) AS manager
  FROM employee;
```

4. Order Matters
```SQL
SELECT track_id, name, milliseconds,
       (CASE
        WHEN milliseconds<=250000 THEN 'Short'
        WHEN milliseconds<=400000 THEN 'Mid length'
        WHEN milliseconds>400000 THEN 'Long'
        ELSE 'Unknown' END) AS length_category
  FROM track;
```

5. CASE BASE Expression
```SQL
SELECT first_name, last_name, title, reports_to,
       (CASE reports_to
         WHEN 1 THEN 'Adams'
         WHEN 2 THEN 'Edwards'
         WHEN 6 THEN 'Mitchell'
         ELSE 'Self'
        END) AS manager
  FROM employee;
```

Assessment
```SQL
SELECT (CASE 
        WHEN milliseconds>300000 THEN 'Long'
        ELSE 'Short' END) AS length_category
  FROM track;
```

```SQL
SELECT (CASE
        WHEN milliseconds>=350000 THEN 'Long'
        WHEN milliseconds>=300000 THEN 'Average'
        ELSE 'Short' END) AS length_category
  FROM track;
```

```SQL
SELECT (CASE
        WHEN milliseconds>350000 THEN 'Long'
        WHEN milliseconds>=300000 THEN 'Average'
        WHEN milliseconds<300000 THEN 'Short' END) AS length_category
  FROM track;
```

```SQL
SELECT customer_id, first_name, last_name,
       (CASE
        WHEN country IN ('Canada', 'USA') THEN 'North America'
        ELSE NULL END) AS continent
  FROM customer
 LIMIT 5;
```

```SQL
SELECT 1;
```
