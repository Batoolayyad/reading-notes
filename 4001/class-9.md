## Introduction to SQL

### What is SQL?


Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.


### What Relational databases?


A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

For example, if the Department of Motor Vehicles had a database, you might find a table containing all the known vehicles that people in the state are driving. This table might need to store the model name, type, number of wheels, and number of doors of each vehicle for example.
 
| Id  	|   Make/Model	 | # Wheels	  | # Doors	| Type         |
|-------|----------------|------------|---------|--------------|
| 1	    | Ford Focus	 | 4	      |4	    | Sedan        |
|2      |Tesla Roadster	 | 4	      |2	    |Sports        |
|3	    |Kawakasi Ninja	 | 2	      |0	    | Motorcycle   |
|4	    |McLaren Formula | 4	      |0        |		Race   |
|5	    |Tesla S	     | 4	      |4	    |Sedan         |


### How SELECT queries?

- To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries

- A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned

```
Select query for a specific columns
SELECT column, another_column, …
FROM mytable;
```

### How to select for specific columns of data from a table?


use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.


```
elect query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```










