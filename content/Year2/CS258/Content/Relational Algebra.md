*We use set semantics in Relational Algebra :(*
## Operators

**Projection ($\pi$)** - 

## Set Theoretic Operators

We can use set-theoretic operations (say for relations $X(A_{1}, \dots, A_{n})$, $Y(B_{1}, \dots, B_{n})$) since we use set semantics in RA ***however*** they require type-compatibility:
- Same number of attributes in each relation: 
- The relations are type-compatible: 

## Cross Joins

Recall that a relation is a set of tuples in the relational model. 

A cross join of two relations $X, Y$ is notated $X \times Y$ and is just the cartesian product from [[Sets|CS130]]! 
As a reminder, $X \times Y = \{(x,y) \; | \; x \in X, \; y \in Y\}$.

The difference is that instead of putting elements in a pair (2-tuple), the elements are concatenated together. The rows from $X, Y$ themselves are tuples, and you add the tuples together like so: 
$A + B = (A_{1}, \; A_{2}, \; \dots , \; A_{n}, \; B_{1}, \; B_{2}, \; \dots, B_{m})$

### Example (for intuition)


### More
More formally, for relations $X(A_{1}, A_{2}, \dots, A_{n})$ and $Y(B_{1}, B_{2}, \dots, B_{m})$ we have:
$X \times Y = \{x + y \; | \; x \in X, \; y \in Y\}$.

We know that the elements in the resulting relation are formed from adding two relations; one of size $n$ from $X$, and one of size $m$ from $Y$. Therefore, there are $n + m$ elements in the resulting relation. We can describe it like so:

$X \times Y = Z(C_{1}, C_{2}, \dots, C_{n+m})$.


```sql
DROP TABLE IF EXISTS Employees; -- ignore this; just so I can rerun it lmao

CREATE TABLE Employees (
  EmployeeID Int PRIMARY KEY,
  Dept varchar(1)
);

INSERT INTO Employees VALUES (1, 'S');
INSERT INTO Employees VALUES (2, 'Q');
INSERT INTO Employees VALUES (3, 'S');

DROP TABLE IF EXISTS Departments;

CREATE TABLE Departments (
  Dept varchar(1) PRIMARY KEY,
  DeptName varchar(10)
);

INSERT INTO Departments VALUES ('S', 'Software');
INSERT INTO Departments VALUES ('Q', 'Quant');

SELECT * FROM (Departments CROSS JOIN Employees) WHERE Departments.Dept = Employees.Dept ORDER BY EmployeeID ASC;

```