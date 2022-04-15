# Code 401 Reading Notes 
### Prework - SQL Practice 

####  source: "Learn SQL", David Fowler, [link](https://landing.chartio.com/download-learn-sql)

```sql 
INSERT INTO books 
(title, author, publication_date, genre)
VALUES ('the poisonwood bible', 'barbara kingsolver', 2005, 'fiction')
```
- id is typically an auto-incrementing integer  
- the line that lists title, author, etc. is optional 

#### source: "SQLBolt", [link](https://sqlbolt.com/)

```sql
SELECT title, author, publication_date, genre, id
FROM books
WHERE publication_date > 2020
AND genre = "Fiction" 
ORDER BY publication_date DESC 
LIMIT 10 
```

```sql 
SELECT title, author, publication_date, domestic_sales
FROM books
INNER JOIN sales
ON books.id = sales.product_id
WHERE publication_date > 2020
```

#### Completion Images: 
## Learn SQL: 
![learn sql ebook](./static/learn-sql-ebook.png)

## SQL Bolt: 
![sql bolt](./static/sql-bolt.png)