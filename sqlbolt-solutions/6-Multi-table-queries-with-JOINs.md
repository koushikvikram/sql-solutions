Find the domestic and international sales for each movie
```SQL
SELECT Title, Domestic_sales, International_sales
FROM movies
JOIN boxoffice 
ON movies.id = boxoffice.movie_id;
```

Show the sales numbers for each movie that did better internationally rather than domestically
```SQL
SELECT Title, Domestic_sales, International_sales
FROM movies
JOIN boxoffice 
ON movies.id = boxoffice.movie_id
WHERE International_sales>Domestic_sales;
```

List all the movies by their ratings in descending order
```SQL
SELECT Title
FROM movies
JOIN boxoffice 
ON movies.id = boxoffice.movie_id
ORDER BY Rating DESC;
```
