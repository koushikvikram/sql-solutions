Run this query to find the first 3 rows of the 'executions' table.

```SQL
SELECT * FROM executions LIMIT 3;
```

Revise the query to select the last_statement column in addition to the existing columns.

```SQL
SELECT first_name, last_name, last_statement
FROM executions
LIMIT 3;
```

Run the given query and observe the error it produces. Fix the query.

```SQL
SELECT first_name FROM executions LIMIT 3;
```

Modify the query to divide 50 and 51 by 2.

```SQL
SELECT 50 / 2, 51 / 2;
```

Verify that messing up capitalization and whitespace still gives a valid query.
```SQL
   SeLeCt   first_name,last_name
  fRoM      executions
           WhErE ex_number = 145;
```

Find the first and last names and ages (ex_age) of inmates 25 or younger at time of execution.

```SQL
SELECT first_name, last_name, ex_age
FROM executions
WHERE ex_age <= 25;
```

Modify the query to find the result for Raymond Landry.

```SQL
SELECT first_name, last_name, ex_number
FROM executions
WHERE first_name LIKE '%Raymond%'
  AND last_name LIKE '%Landry%';
```

Insert a pair of parenthesis so that this statement returns 0.

```SQL
SELECT 0 AND (0 OR 1);
```

Select the WHERE blocks with valid clauses.
- WHERE 0
- WHERE ex_number < ex_age
- WHERE ex_age

Find Napoleon Beazley's last statement.

```SQL
SELECT last_statement
FROM executions
WHERE first_name LIKE '%Napoleon%' AND 
      last_name LIKE '%Beazley%';
```
