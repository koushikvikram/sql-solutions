1. Introduction
```SQL
SELECT invoice_id, invoice_date, billing_country, total
  FROM invoice 
 LIMIT 3;
```

2. Column Sum
```SQL
SELECT SUM(total) AS overall_sale
  FROM invoice;
```

3. Column Average
```SQL
SELECT AVG(total) AS avg_sale
  FROM invoice;
```

4. Minimum and Maximum Values in a Numeric Column
```SQL
SELECT MAX(total) AS max_sale
  FROM invoice;
```

5. First and Last Values in a Text Column
```SQL
SELECT MAX(billing_country) AS last_billing_country
  FROM invoice;
```

6. Counting Rows
```SQL
SELECT COUNT(*) AS num_rows
  FROM invoice;
```

7. Counting Rows with Missing Values
```SQL
SELECT COUNT(composer) AS num_composers
  FROM track;
```

Assessment
```SQL
SELECT SUM(total) AS overall_sum
  FROM invoice;
```

```SQL
SELECT MAX(quantity) AS max_quantity
  FROM invoice_line;
```

```SQL
SELECT 2, 3;
```

```SQL
SELECT COUNT(*) AS num_albums
  FROM album;
```

```SQL
SELECT 1, 4, 5;
```
