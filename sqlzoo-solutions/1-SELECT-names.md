1. Find the country that starts with Y.
```SQL
SELECT name FROM world
WHERE name LIKE 'Y%';
```

2. Find the countries that end with y.
```SQL
SELECT name FROM world
WHERE name LIKE '%Y';
```

3. Find the countries that contain the letter x.
```SQL
SELECT name FROM world
WHERE name LIKE '%X%';
```

4. Find the countries that end with land.
```SQL
SELECT name FROM world
WHERE name LIKE '%LAND';
```

5. Find the countries that start with C and end with ia.
```SQL
SELECT name FROM world
WHERE name LIKE 'C%IA';
```

6. Find the country that has oo in the name,
```SQL
SELECT name FROM world
WHERE name LIKE '%OO%';
```

7. Find the countries that have three or more a in the name.
```SQL
SELECT name FROM world
WHERE name LIKE '%A%A%A%';
```

8. Find the countries that have "t" as the second character.
```SQL
SELECT name FROM world
WHERE name LIKE '_t%'
ORDER BY name;
```

9. Find the countries that have two "o" characters separated by two others.
```SQL
SELECT name FROM world
WHERE name LIKE '%o__o%';
```

10. Find the countries that have exactly four characters.
```SQL
SELECT name FROM world
WHERE name LIKE '____';
```

11. Find the country where the name is the capital city.
```SQL
SELECT name
FROM world
WHERE name = capital;
```

12. Find the country where the capital is the country plus "City".
```SQL
SELECT name
FROM world
WHERE capital = CONCAT(name, ' City');
```

13. Find the capital and the name where the capital includes the name of the country.
```SQL
SELECT capital, name
FROM world
WHERE capital LIKE CONCAT('%', name, '%');
```

14. Find the capital and the name where the capital is an extension of name of the country. You should include Mexico City as it is longer than Mexico. You should not include Luxembourg as the capital is the same as the country.
```SQL
SELECT capital, name
FROM world
WHERE capital LIKE CONCAT(name, '_%');
```

15. Show the name and the extension where the capital is an extension of name of the country.
For Monaco-Ville the name is Monaco and the extension is -Ville.
```SQL
SELECT name, REPLACE(capital, name, '') AS extension
FROM world
WHERE capital LIKE CONCAT(name, '_%');
```
