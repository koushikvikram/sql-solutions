1. Ordering Results
```SQL
SELECT name, milliseconds
  FROM track
 ORDER BY milliseconds;
```

2. Limiting Results
```SQL
SELECT name, milliseconds
  FROM track
 ORDER BY milliseconds
 LIMIT 3;
```

3. Ordering by Multiple Columns
```SQL
SELECT employee_id, first_name, last_name, reports_to
  FROM employee
 ORDER BY reports_to, last_name;
```

4. Reversing the Order
```SQL
SELECT customer_id, first_name, last_name, country
  FROM customer
 ORDER BY country DESC, first_name, last_name;
```

5. Not Including Ordering Columns
```SQL
SELECT invoice_id
  FROM invoice
 ORDER BY total DESC
 LIMIT 5;
```

6. Order by Expressions
```SQL
SELECT customer_id, first_name, last_name, country,
       (CASE country
        WHEN 'Canada' THEN 0
        WHEN 'USA' THEN 1
        ELSE 2 END) AS country_id
  FROM customer
 ORDER BY country_id, country;
```

7. The Order of Execution
```SQL
SELECT 6;
```

Assessment
```SQL
SELECT 3;
```

```SQL
SELECT *
  FROM track
 ORDER BY milliseconds;
```

```SQL
SELECT *
  FROM track
 ORDER BY bytes DESC;
```

```SQL
SELECT track_id, name, bytes, milliseconds, unit_price
  FROM track
 ORDER BY CAST(bytes AS REAL)/milliseconds DESC;
```

```SQL
SELECT *
  FROM employee
 ORDER BY city, hire_date;
```
