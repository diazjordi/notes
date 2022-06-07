# BASIC COMMANDS

Pull everything from a table

```SQL
SELECT *
FROM table_name
```

Pull everything that is unique in relation to specified `DISTINCT` column

```SQL
SELECT DISTINCT column1
FROM table_name
```

Pull everything from a table matching parameters in `WHERE` clause

- column = 'text value'
- column = numeric value

|Operator|Description|
|:---    |:---       |
|=       |Equal|
|>       |Greater Than|
|<       |Less Than|
|>=      |Greater than or equal|
|<=      |Less than or equal|
|<>      |Not equal, sometimes used as "!="|
|BETWEEN |Between a certain range|
|LIKE    |Search for a pattern|
|IN      |To specify multiple possible values for a column|

```SQL
SELECT column1, column2
FROM table_name
WHERE condition = "VALUE"
```

AND, OR, NOT Syntax

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;

SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;

SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

ORDER BY

```SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;

SELECT * FROM Customers
ORDER BY Country, CustomerName;
```

INSERT INTO

- first method you specify both the column names and the values to be inserted

```SQL
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');
```

- second method if you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows

```SQL
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

