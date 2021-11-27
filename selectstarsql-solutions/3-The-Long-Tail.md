This query pulls the execution counts per county.
```SQL
SELECT county, COUNT(*) AS county_executions
FROM executions
GROUP BY county;
```

Modify this query so there are up to two rows per county — one counting executions with a last statement and another without.
```SQL
SELECT
  county,
  last_statement IS NOT NULL AS last_statement_present,
  COUNT(*)
FROM executions
GROUP BY county, last_statement_present
```

Count the number of inmates aged 50 or older that were executed in each county.
```SQL
SELECT county, COUNT(*) 
FROM executions
WHERE ex_age >= 50
GROUP BY county;
```

List the counties in which more than 2 inmates aged 50 or older have been executed.
```SQL
SELECT county
FROM executions
WHERE ex_age>=50
GROUP BY county
HAVING COUNT(*)>2;
```

Mark the statements that are true.
This query finds the number of inmates from each county and 10 year age range.
```
SELECT
    county,
    ex_age/10 AS decade_age,
    COUNT(*)
FROM executions
GROUP BY county, decade_age;
```
Correct Options:
- The query is valid (ie. won't throw an error when run).
  - The query would return more rows if we were to use **ex_age** instead of **ex_age/10**.
- The output will have as many rows as there are unique combinations of counties and decade_ages in the dataset.
- The query would be valid even if we don't specify county in the **SELECT** block.

Incorrect Options:
- The output will have a group ('Bexar', 6) even though no Bexar county inmates were between 60 and 69 at execution time.
- The output will have a different value of county for every row it returns.
- The output can have groups where the count is 0.
- It is reasonable to add **last_name** to the **SELECT** block even without grouping by it.

List all the distinct counties in the dataset. Stick with vanilla SELECT and use GROUP BY.
```SQL
SELECT county
FROM executions
GROUP BY county;
```

Find the first and last name of the the inmate with the longest last statement (by character count).
```SQL
SELECT first_name, last_name
FROM executions
WHERE LENGTH(last_statement) =
    (SELECT MAX(LENGTH(last_statement))
	 FROM executions)
```

Insert the <count-of-all-rows> query to find the percentage of executions from each county.

```SQL
SELECT
  county,
  100.0 * COUNT(*) / (SELECT COUNT(*) FROM executions)
    AS percentage
FROM executions
GROUP BY county
ORDER BY percentage DESC
```
