## What is SQL database
Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database.

## Lesson 1 : SELECT queries 101

 ***Select spicific column/s from mytable*** <br>
<pre>SELECT column, another_column, …etc
FROM mytable;</pre> 
<br>

 ***Select all columns from mytable*** <br>
<pre>SELECT *
FROM mytable;  </pre> 

### Lesson 2 : Queries with constraints (Pt. 1)

***Select query with constraints***
<pre>SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;</pre>
![Condition Table]()
