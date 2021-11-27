Find the movie with a row id of 6
```SQL
SELECT Title 
FROM movies
WHERE Id=6;
```

Find the movies released in the years between 2000 and 2010
```SQL
SELECT Title 
FROM movies
WHERE Year>2000 AND YEAR<=2010;
```

Find the movies not released in the years between 2000 and 2010
```SQL
SELECT Title 
FROM movies
WHERE NOT (Year>2000 AND YEAR<=2010);
```

Find the first 5 Pixar movies and their release year
```SQL
SELECT Title, Year
FROM movies
LIMIT 5;
```
