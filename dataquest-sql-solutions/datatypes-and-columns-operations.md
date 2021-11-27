1. Storage Classes
```SQL
SELECT 'Integer', 'Text', 'Text', 'Real';
```

2. Operations with Text
```SQL
SELECT 'John' || 'Doe' AS name;
```

3. Aliases
```SQL
SELECT first_name, phone 
    AS work_phone
  FROM employee;
```

4. Operations Between Columns and Strings
```SQL
SELECT first_name || ' Chinook' 
    AS first_name_chinook
  FROM employee;
```

5. Operations with Text Columns
```SQL
SELECT first_name || ' ' || last_name 
    AS full_name
  FROM employee;
```

6. Challenge! - Operations with Numeric Columns
```SQL
SELECT unit_price*quantity AS total_line,
       unit_price*0.85 AS unit_price_eur
  FROM invoice_line
 LIMIT 5;
```

Assessment
```SQL
SELECT 'Media:' || name 
  FROM media_type;
```

```SQL
SELECT 'Playlist:' || name AS playlist_name
  FROM playlist;
```

```SQL
SELECT employee_id, last_name || ', ' || first_name AS name, title, reports_to
  FROM employee
 LIMIT 8; 
```

```SQL
SELECT 'Text', 'Text', 'Integer';
```

```SQL
SELECT track_id, name, bytes*8 AS bits
  FROM track
 LIMIT 5;
```
