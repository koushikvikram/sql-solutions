The director for A Bug's Life is incorrect, it was actually directed by John Lasseter
```SQL
UPDATE movies
SET Director='John Lasseter'
WHERE Title='A Bug''s Life';
```

The year that Toy Story 2 was released is incorrect, it was actually released in 1999
```SQL
UPDATE movies
SET Year=1999
WHERE Title='Toy Story 2';
```

Both the title and director for Toy Story 8 is incorrect! The title should be "Toy Story 3" and it was directed by Lee Unkrich
```SQL
UPDATE movies
SET Title='Toy Story 3', Director='Lee Unkrich'
WHERE Id=11;
```
