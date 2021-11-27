1. The Order of Execution
```SQL
SELECT *
  FROM employee
 WHERE reports_to=2
 LIMIT 2;
 ```
 
 2. Comparison Operators
 ```SQL
 SELECT employee_id, last_name, first_name, title, reports_to, hire_date
  FROM employee
 WHERE SUBSTRING(hire_date, 1, 4) <> '2016';
 ```
 
 3. Comparing Numbers: Greater Than
 ```SQL
 SELECT name
  FROM track
 WHERE ((CAST(milliseconds AS REAL)/1000)/60)>60;
 ```
 
 4. Comparing Number: Greater than or Equal to
 ```SQL
 SELECT *
  FROM invoice
 WHERE total>=18.81;
 ```
 
 5. Between two values
 ```SQl
 SELECT *
  FROM track
 WHERE CAST(milliseconds AS REAL)/1000/60 BETWEEN 17 AND 19;
 ```
 
Assessment
```SQL
SELECT *
  FROM employee
 WHERE NOT SUBSTRING(first_name, 1, 1)='M';
```

```SQL
SELECT name
  FROM track
 WHERE milliseconds>=300000;
```

```SQL
SELECT 4;
```

```SQL
SELECT name
  FROM track
 WHERE milliseconds<60000 OR milliseconds>=3600000;
```

```SQL
SELECT *
  FROM invoice
 WHERE total BETWEEN 4.95 AND 7;
```
