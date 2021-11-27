Find the number of movies each director has directed
```SQL
SELECT director, COUNT(title) 
FROM movies
GROUP BY director;
```

Find the total domestic and international sales that can be attributed to each director
```SQL
SELECT director, SUM(domestic_sales+international_sales) AS total_sales
FROM movies JOIN boxoffice
ON movies.id=boxoffice.movie_id
GROUP BY director;
```
