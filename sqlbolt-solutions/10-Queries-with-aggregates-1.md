Find the longest time that an employee has been at the studio
```SQL
SELECT MAX(years_employed) AS longest_time_at_studio
FROM employees;
```

For each role, find the average number of years employed by employees in that role
```SQL
SELECT role, AVG(years_employed) AS average_years_employed
FROM employees
GROUP BY role;
```

Find the total number of employee years worked in each building
```SQL
SELECT building, SUM(years_employed) AS total_employee_years
FROM employees
GROUP BY building;
```
