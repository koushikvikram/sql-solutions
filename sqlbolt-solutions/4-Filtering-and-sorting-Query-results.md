List all directors of Pixar movies (alphabetically), without duplicates
```SQL
SELECT DISTINCT Director
FROM movies
ORDER BY Director ASC;
```

List the last four Pixar movies released (ordered from most recent to least)
```SQL
SELECT Title
FROM movies
ORDER BY Year DESC
LIMIT 4;
```

List the first five Pixar movies sorted alphabetically
```SQL
SELECT Title
FROM movies
ORDER BY Title ASC
LIMIT 5;
```

List the next five Pixar movies sorted alphabetically
```SQL
SELECT Title
FROM movies
ORDER BY Title ASC
LIMIT 5 OFFSET 5;
```
