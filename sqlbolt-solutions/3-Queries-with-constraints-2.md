Find all the Toy Story movies
```SQL
SELECT Title 
FROM movies
WHERE Title LIKE '%Toy Story%';
```

Find all the movies directed by John Lasseter
```SQL
SELECT Title 
FROM movies
WHERE Director='John Lasseter';
```

Find all the movies (and director) not directed by John Lasseter
```SQL
SELECT Title, Director
FROM movies
WHERE NOT Director='John Lasseter';
```

Find all the WALL-* movies
```SQL
SELECT Title
FROM movies
WHERE Title LIKE 'WALL-%';
```
