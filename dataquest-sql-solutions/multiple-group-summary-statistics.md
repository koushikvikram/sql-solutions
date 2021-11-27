1. Introduction
```SQL
SELECT billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale
  FROM invoice
 WHERE billing_country='USA'
 GROUP BY billing_state;
```

2. Grouping over Several Columns 
```SQL
SELECT billing_country, billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale
  FROM invoice
 GROUP BY billing_country, billing_state;
```

3. Adding Conditions on an Aggregated Column: the Correct Way
```SQL
SELECT billing_country, billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale 
  FROM invoice
 GROUP BY billing_country, billing_state
 HAVING COUNT(*) > 40;
```

4. Revisiting the Order of Execution
```SQL
SELECT 2, 3, 6;
```

5. Adding Conditions on Not-Displayed Aggregate Column
```SQL
SELECT MIN(total) AS min_sale, MAX(total) AS max_sale
  FROM invoice
 GROUP BY billing_country, billing_state
 HAVING AVG(total)<10;
```

6. Combining WHERE and HAVING Clauses
```SQL
SELECT billing_country, billing_state, MIN(total) AS min_sale, MAX(total) AS max_sale 
  FROM invoice
 WHERE NOT billing_state='None'
 GROUP BY billing_country, billing_state
HAVING AVG(total) < 10;
```

Assessment
```SQL
SELECT city, country, COUNT(*) AS num_rows, MAX(last_name) AS last_last_name
  FROM customer
 GROUP BY city, country
 LIMIT 3;
```

```SQL
SELECT 1;
```

```SQL
SELECT invoice_date, MIN(total) AS min_purchase_amount, MAX(total) AS max_purchase_amount, SUM(total) AS total_purchase_amount, AVG(total) AS avg_purchase_amount
  FROM invoice
 GROUP BY invoice_date
HAVING MIN(total)>=15;
```

```SQL
SELECT customer_id, AVG(total) AS avg_purchase_amount
  FROM invoice
 WHERE billing_country='USA'
 GROUP BY customer_id
HAVING SUM(total) BETWEEN 50 AND 75;
```

```SQL
SELECT invoice_date, COUNT(*) AS num_invoices
  FROM invoice
 GROUP BY invoice_date
HAVING COUNT(*)>=4;
```
