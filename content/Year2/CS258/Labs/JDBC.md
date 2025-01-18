Some common places to go wrong:

>[!warning]- The connection attempt failed
>You typically get this when you run the JDBC, but the Postgres server isn't running.
>
>Make sure the Postgres server has started!
## Prepared Statements

SQL :)


```java
PreparedStatement exampleStmt = conn.prepareStatement("SELECT * FROM relation;");
```
We distinguish two types of SQL command:
- Query (returns stuff to view)
- Update (returns number of rows changed)

### Query Prepared Statements

### Update Prepared Statements

### Using setInt(), setString() etc.

These provide additional security against attacks like SQL injection.

## Representing NULL

Different types have different ways of inserting "NULL".
You use **setNull(parameterId, aNull)** where **aNull** varies from type to type. 

