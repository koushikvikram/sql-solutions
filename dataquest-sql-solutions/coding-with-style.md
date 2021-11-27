1. Coding Comments
```SQL
SELECT *
  FROM genre
 LIMIT 5; -- take only the first 5 rows
```

2. Block Comments
```SQL
/*
Show the first 5 rows from the invoice_line table
*/
SELECT *
  FROM invoice_line
 LIMIT 5;
```

3. Reserved Words
```SQL
SELECT media_type_id, name
  FROM media_type
 LIMIT 1;
```

4. Coding with Style
```SQL
SELECT customer_id, first_name, last_name, email 
FROM customer 
LIMIT 5;
```

5. Rivers
```SQL
SELECT * 
  FROM artist 
 LIMIT 10;
```

Assessment
```SQL
SELECT first_name, last_name
  FROM customer
 LIMIT 7; -- take only the first 7 rows
```

```SQL
/* take a look at the 
first 5 rows in the 
employee table
*/
SELECT *
  FROM employee
 LIMIT 5;
```

```SQL
SELECT * 
  FROM invoice_line 
 LIMIT 10;
```

```SQL
SELECT title, reports_to, hire_date 
  FROM employee 
 LIMIT 10;
```

```SQL
SELECT city, state, country, postal_code
  FROM employee
 LIMIT 20;
```
