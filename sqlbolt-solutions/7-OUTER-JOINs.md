Find the list of all buildings that have employees
```SQL
SELECT DISTINCT building 
FROM employees JOIN buildings
ON employees.building=buildings.building_name;
```

Find the list of all buildings and their capacity
```SQL
SELECT DISTINCT building_name, capacity 
FROM buildings LEFT JOIN employees
ON buildings.building_name=employees.building;
```

List all buildings and the distinct employee roles in each building (including empty buildings)
```SQL
SELECT DISTINCT building_name, role 
FROM buildings LEFT JOIN employees
ON buildings.building_name=employees.building;
```
