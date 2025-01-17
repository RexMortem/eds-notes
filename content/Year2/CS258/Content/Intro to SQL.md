## Declarative over Procedural
The DB System philosophy: *"Tell the DBS what you want"*.

**Data Manipulation Languages (DMLs)** are for querying/updating data and should be **declarative**; say what you want, but not how to do it. 
Why? **Query Optimisation:** the DBS will find an optimal (or close to) way to execute query. 

**Data Definition Languages (DDLs)** are for defining the DB. 

## 

## Content to be organised later
```sql
SELECT CU.first_name AS fn, CU.age AS ag, CU.age*2 AS doubledAge
FROM Customers AS CU WHERE ag > 25;

-- American query
SELECT C.first_name 'First Name', 'American''s!' Nationality FROM Customers C WHERE C.country='USA';
```

REMEMBER Create Table is a statement, requiring a ;

Scalar Subquery error:
```
ERROR:  more than one row returned by a subquery used as an expression

```