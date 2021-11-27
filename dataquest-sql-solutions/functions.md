1. Functions
```SQL
SELECT ROUND(2.58, 0) AS nearest_unit;
```

2. Multiple Inputs
```SQL
SELECT ROUND(1.3378, 2) AS round_hundredth;
```

3. Columns as Arguments
```SQL
SELECT invoice_id, customer_id, ROUND(total, 0) AS rounded_total
  FROM invoice
 LIMIT 10;
```

4. Results of Functions as Arguments
```SQL
SELECT ROUND(unit_price*0.85, 2) AS unit_price_eur, 
       LENGTH(ROUND(unit_price*0.85, 2)) AS len_unit_price_eur
  FROM invoice_line
 LIMIT 5;
```

5. Integer Division
```SQL
SELECT (milliseconds/1000)/60 AS integer_minutes,
       (CAST(milliseconds AS REAL)/1000)/60 AS float_minutes
FROM track
LIMIT 10;
```

6. String Functions I - UPPER and LOWER
```SQL
SELECT LOWER(last_name) AS lowercase_last_name
  FROM employee;
```

7. String Functions II - SUBSTRING
```SQL
SELECT SUBSTRING(first_name, 1, 3) AS first_three_letters
  FROM employee; 
```

8. String Functions III - REPLACE
```SQL
SELECT REPLACE((first_name || ' ' || last_name), 's', '$') AS full_name
FROM employee;
```

Assessment
```SQL
SELECT SUBSTRING(name, 1, 5) AS short_name
  FROM artist;
```

```SQL
SELECT 1;
```

```SQL
SELECT 4;
```

```SQL
SELECT track_id, name, CAST(bytes AS REAL)/1000000 AS megabytes
  FROM track
 LIMIT 5; 
```

```SQL
SELECT ROUND(CAST(bytes AS REAL)/1000000, 2) AS megabytes
  FROM track;
```
