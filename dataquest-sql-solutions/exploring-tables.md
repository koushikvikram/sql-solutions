1. Previewing Results
```SQL
SELECT *
FROM invoice_line
LIMIT 10;
```

2. The Order of Clauses
```SQL
FROM invoice_line
SELECT *
 LIMIT 5
 ```

3. The Order of Execution
```SQL
SELECT 2;
```

4. Unique Rows
```SQL
SELECT DISTINCT unit_price
FROM invoice_line;
```

5. SQL Dialects
```
SELECT invoice_id, track_id
FROM invoice_line
LIMIT 3;
```

Assessment
```SQL
SELECT *
FROM invoice_line
LIMIT 2;
```

```SQL
SELECT quantity, unit_price, invoice_id
FROM invoice_line
LIMIT 10
```

```SQL
SELECT *
FROM invoice_line
LIMIT 670;
```

```SQL
SELECT 3;
```

```SQL
SELECT *
FROM artist
LIMIT 0;
```
