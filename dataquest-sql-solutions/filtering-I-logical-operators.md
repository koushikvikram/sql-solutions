1. Expressions
```SQL
SELECT *
  FROM employee
 LIMIT 5;
```

2. Filtering Results with WHERE
```SQL
SELECT *
  FROM employee
 LIMIT 5;
```

3. Expression in WHERE
```SQL
SELECT *
  FROM employee
 WHERE LENGTH(first_name)=LENGTH(last_name);
```

4. Conditions
```SQL
SELECT *
  FROM employee
 WHERE 1=1;
```

5. NOT Equal
```SQL
SELECT *
  FROM employee
 WHERE NOT SUBSTRING(birthdate, 1, 4)='1973';
```

6. Multiple Conditions I
```SQL
SELECT *
  FROM employee
 WHERE SUBSTRING(first_name, 1, 1)='M' AND SUBSTRING(hire_date, 1, 4)='2016';
```

7. Multiple Conditions II
```SQL
SELECT *
  FROM employee
 WHERE (LENGTH(first_name)=5 OR LENGTH(first_name)=6) 
       AND SUBSTRING(hire_date, 1, 4)='2017';
```

Assessment
```SQL
SELECT 0;
```

```SQL
SELECT *
  FROM invoice
 WHERE billing_city='Chicago';
```

```SQL
SELECT 0;
```

```SQL
SELECT *
  FROM employee
 WHERE NOT city='Calgary';
```

```SQL
SELECT 10;
```
