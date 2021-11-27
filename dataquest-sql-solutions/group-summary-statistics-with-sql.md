1. Introduction
```SQL
SELECT COUNT(*) AS num_row
  FROM invoice
 WHERE billing_country='USA';
```

2. Counting Rows by Group
```SQL
SELECT billing_country, COUNT(*) AS num_row
  FROM invoice
 GROUP BY billing_country;
```

3. Summary Statistics by Group
```SQL
SELECT invoice_id, SUM(unit_price*quantity) AS total
  FROM invoice_line
 GROUP BY invoice_id
 LIMIT 5;
```

4. Revisiting the Order of Clauses
```SQL
SELECT 2, 3, 6;
```

5. Revisiting the Order of Execution
```SQL
SELECT 3, 5, 6;
```

6. Summary Statistics by Group Under Conditions
```SQL
SELECT billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale
  FROM invoice
 WHERE billing_country='USA'
 GROUP BY billing_state;
```

7. Summary Statistics by Ordered Groups
```SQL
SELECT track_id, COUNT(*) AS num_row, SUM(unit_price*quantity) AS overall_sale
  FROM invoice_line
 GROUP BY track_id
 ORDER BY overall_sale DESC, num_row DESC
 LIMIT 5;
```

Assessment
```SQL
SELECT reports_to, COUNT(reports_to) AS num_reports
  FROM employee
 GROUP BY reports_to;
```

```SQL
SELECT 3;
```

```SQL
SELECT reports_to, MIN(first_name) AS first_report_first_name
  FROM employee
 WHERE title LIKE 'IT%'
 GROUP BY reports_to;
```

```SQL
SELECT track_id, COUNT(*) AS num_track_sold
  FROM invoice_line
 GROUP BY track_id
 ORDER BY num_track_sold DESC
 LIMIT 3;
```

```SQL
SELECT track_id, COUNT(*) AS num_track_sold
  FROM invoice_line
 WHERE unit_price=0.99
 GROUP BY track_id
 ORDER BY num_track_sold
 LIMIT 5;
```
