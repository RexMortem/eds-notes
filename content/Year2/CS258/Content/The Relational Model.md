## Quick Informal Defs for Relational Model

**Relation:** a table of values, with:
- **rows** where elements represent real-world facts 
- **columns** which represent a property 

A **key** of a relation:
- makes a row uniquely identifiable 
- may be an assigned sequential number (**artificial**/**surrogate** key)

A **schema** is a description of a relation:
- name of relation
- name of attributes of relation
- **Example:** Students(StudentId, StudentName, Grade, Age) *describes relation* Students
## Key Facts 

## Relational Model 

A **relation** is a table of values, like below:

| oStudentID | Grade | Age |
| ---------- | ----- | --- |
|            |       |     |
|            |       |     |
|            |       |     |
|            |       |     |

A **relation** is a **set** of tuples including:
- rows which are called ***tuples*** (denoted by $<\dots>$ in CS258)
- columns, called ***attributes***

Each attribute:
- has a set of valid values (or a **domain**)
	- For example, the domain of Grade may be $\{0, 1, 2, \dots , 100\}$
	- Domains also often have formats 
	
Each tuple: 
- has data elements that correspond to real-world data 
	- has a value from the domain of the attribute
- is uniquely identifiable (by the key)
	- An assigned ID (which can be a sequential number) are called ***artificial*** or ***surrogate***

The set of rows is also called a relation's state. 
- state $\subseteq a_{1} \times a_{2} \times \dots \times a_{n}$ where $a_{i}$ is the domain of the corresponding attribute.  

You might ask about the headers, since they appear to be the first tuple in the relation.  
The headers are called ***attribute names***, and they are for interpreting the data elements.

### Schema

The **Schema** of a relation is a description, in the form $RELATION(A1, A2, \dots, A_{n})$. 
For example, the schema for the above relation is $STUDENT(StudentID, \; Grade, \; Age)$.

## Relational DB Constraints 

### Key Constraints 

### Entity Integrity Constraints 

Why should all info not be stored in one table? 
	- Lots of redundant data 

