>[!warning]- Formal Terms and SQL Terms
>In the module, we learn formal/theory terms from learning the Relational Model.
>In SQL, we have different terms for the things inside the Relational Model.
> 
>This is something you'll see a lot in databases and you'll just have to get used to all duplicate terms! 
>In PSQL, we see **both** the formal terms and SQL terms. *yayyyy*
>
>In the Relational Model, we talk about **Relations**, **Tuples**, and **Attributes**.
>In SQL, we talk about **Tables**, **Rows**, and **Columns**.

>[!warning]- Why you should end lines with semicolons
>When you are in PSQL, you should **almost always** end your lines with ';'
>
>If you don't, then the command will either:
>- be executed immediately (and correctly) if it starts with a backslash e.g. `\dt`, `\i`, `\list`
>- put in a buffer
>  
>  The dangerous case is when it's put in a buffer.
>  Commands will be dumped into the buffer *until* a semicolon is encountered at the end of a buffer-able command.
>  So the following situation could happen:
>  ```bash
>  aDatabase=# aMistake
>  aDatabase=# SELECT \* FROM aRelation; 
>  ERROR: syntax error at or near "aMistake"
>  LINE 1: aMistake
>        ^
>  ```
>  
>  If you've had a bunch of commands in-between, then this might come as a shock; you seemingly entered a valid command and it *looks* like psql hallucinated "aMistake" out of nowhere. 
>  
>  What's actually happened in the above is that the command `aMistakeSELECT * FROM aRelation;` was executed, because `aMistake` was added to the before due to the missing semicolon. 
>  
>  **Cool follow-on:** You can actually enter commands across many lines, by not clearing the buffer on purpose. So you can do:
>  ```bash
>  aDatabase=# SELECT
>  aDatabase=# *
>  aDatabase=# FROM aRelation;
>  ```
>  which will work fine. 
>  
>  **Moral of the story:** Please don't forget your semicolon!

 
## Databases

**create database dbName** - create a database with name *dbName*
**\c dbName** - connect to database with name *dbName*
**\list** - lists the databases (and various properties)
## Running SQL

**\i sqlFile** - runs (or **i**nterprets) the SQL file on the database