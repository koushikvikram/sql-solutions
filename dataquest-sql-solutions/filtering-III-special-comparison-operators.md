1. LIKE
```SQL
SELECT phone
  FROM customer
 WHERE first_name LIKE '%belle%';
```

2. Patterns
```SQL
SELECT first_name, last_name
  FROM customer
 WHERE first_name LIKE '%a%a%a%' OR first_name LIKE '%A%A%A%';
```

3. IN a list
```SQL
SELECT *
  FROM customer
 WHERE state IN ('CT', 'DE', 'FL', 'GA', 'MA', 'MD', 'ME',
 'NC', 'NH', 'NJ', 'NY', 'RI', 'SC', 'VA');
```

4. Comparing with Missing Values
```SQL
SELECT 0;
```

5. A Stronger Equality
```SQL
SELECT employee_id, last_name, first_name, title, reports_to
  FROM employee
 WHERE reports_to <> 1 OR reports_to IS NULL;
```

Assessment
```SQL
SELECT first_name, last_name
  FROM customer
 WHERE first_name LIKE 'd%n';
```

```SQL
SELECT name
  FROM track
 WHERE name LIKE '% % %';
```

```SQL
SELECT *
  FROM customer
 WHERE country IN ('Argentina', 'Australia', 'Brazil', 'Chile', 'India');
```

```SQL
SELECT 0;
```

```SQL
SELECT *
  FROM customer
 WHERE state IS NULL;
```
