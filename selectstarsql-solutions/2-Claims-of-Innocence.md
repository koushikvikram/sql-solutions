Edit the query to find how many inmates provided last statements.

```SQL
SELECT COUNT(last_statement) FROM executions;
```

Verify that 0 and the empty string are not considered NULL.

```SQL
SELECT (0 IS NOT NULL) AND ('' IS NOT NULL) ;
```

Find the total number of executions in the dataset.

```SQL
SELECT COUNT(first_name) FROM executions;
```

Verify that COUNT(*) gives the same result as before.

```SQL
SELECT COUNT(*) FROM executions;
```

This query counts the number of Harris and Bexar county executions. Replace SUMs with COUNTs and edit the CASE WHEN blocks so the query still works.

```SQL
SELECT
    COUNT(CASE WHEN county='Harris' THEN 1
        ELSE NULL END),
    COUNT(CASE WHEN county='Bexar' THEN 1
        ELSE NULL END)
FROM executions;
```

Find how many inmates were over the age of 50 at execution time.

```SQL
SELECT COUNT(ex_age) 
FROM executions
WHERE ex_age>50;
```

Find the number of inmates who have declined to give a last statement.
- With a WHERE block
```SQL
SELECT COUNT(*) 
FROM executions
WHERE last_statement IS NULL;
```
- With a COUNT and CASE WHEN block
```SQL
SELECT COUNT(CASE WHEN last_statement IS NULL THEN 1 ELSE NULL END)
FROM executions;
```
- With two COUNT functions
```SQL
SELECT COUNT(*)-COUNT(last_statement)
FROM executions;
```

Find the minimum, maximum and average age of inmates at the time of execution.

```SQL
SELECT MIN(ex_age), MAX(ex_age), AVG(ex_age) 
FROM executions;
```

Find the average length (based on character count) of last statements in the dataset.

```SQL
SELECT AVG(LENGTH(last_statement))
FROM executions;
```

List all the counties in the dataset without duplication.

```SQL
SELECT DISTINCT county
FROM executions;
```

Find the proportion of inmates with claims of innocence in their last statements.

```SQL
SELECT COUNT(CASE 
		WHEN last_statement LIKE '%innocent%' THEN 1
		ELSE NULL
	     END)*1.0/COUNT(*)
FROM executions;
```
```SQL
SELECT SUM(last_statement LIKE '%innocent%')*1.0/COUNT(*)
FROM executions;
```
