List all the Canadian cities and their populations
```SQL
SELECT City, Population 
FROM north_american_cities
WHERE Country='Canada';
```

Order all the cities in the United States by their latitude from north to south
```SQL
SELECT City
FROM north_american_cities
WHERE Country='United States'
ORDER BY latitude DESC;
```

List all the cities west of Chicago, ordered from west to east
```SQL
SELECT City
FROM north_american_cities
WHERE Longitude<-87.629798
ORDER BY Longitude ASC;
```

List the two largest cities in Mexico (by population)
```SQL
SELECT City
FROM north_american_cities
WHERE Country='Mexico'
ORDER BY Population DESC
LIMIT 2;
```

List the third and fourth largest cities (by population) in the United States and their population
```SQL
SELECT City
FROM north_american_cities
WHERE Country='United States'
ORDER BY Population DESC
LIMIT 2 OFFSET 2;
```
