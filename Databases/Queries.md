# Query

## Estructura básica de un query

`SELECT` city, COUNT(\*) `AS` total
`FROM` people
`WHERE` active = true
`GROUP BY` city
`ORDER BY` total `DESC`
`HAVING` total >= 2;
