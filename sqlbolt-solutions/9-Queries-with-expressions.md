List all movies and their combined sales in millions of dollars
```SQL
SELECT title, (domestic_sales+international_sales)/1000000 AS total_sales_in_millions
FROM movies JOIN boxoffice
ON movies.id=boxoffice.movie_id;
```

List all movies and their ratings in percent
```SQL
SELECT title, rating*10 AS rating_in_percent
FROM movies JOIN boxoffice
ON movies.id=boxoffice.movie_id;
```

List all movies that were released on even number years
```SQL
SELECT Title
FROM Movies
WHERE Year%2==0;
```
