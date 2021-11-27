Find the number of Artists in the studio (without a HAVING clause)
```SQL
SELECT COUNT(*) 
FROM employees
WHERE Role='Artist';
```

Find the number of Employees of each role in the studio
```SQL
SELECT COUNT(*) 
FROM employees
WHERE Role='Artist';
```

Find the total number of years employed by all Engineers
```SQL
SELECT SUM(years_employed) 
FROM employees
WHERE Role='Engineer';
```
