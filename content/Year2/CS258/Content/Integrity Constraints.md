These are constraints that control what is a valid state for relations, hence "integrity". 

We will discuss:

>[!info]- More Terminology
>Some more terms (yay!) to help with understanding
> 
>**Entity** - thing recorded in a databases; represented by a table/relation
>**Instance of an entity** - a row/tuple of a table

## Domain Constraints

This is a constraint on attributes; values can only be from the domain of an attribute.

For example, an INT attribute can't contain a string. 

## Entity Integrity Constraints

Entity Integrity is about the attributes being not NULL.
A key example: the attributes that form the Primary Key (PK) cannot be NULL. 

**Note:** you may see this defined differently in other places; sometimes entity integrity is about the uniqueness of data. In this module, that uniqueness property is called the **Key Constraint**

## Referential Integrity Constraints

These are constraints about interactions between tables. 

Generally referential integrity is respected by:
- allowing only references to relations, and PKs, that exist
- allowing only values that are either:
	- NULL
	- a value that exists in the other (foreign) relation

Keep in mind that you have to also respect the Domain Constraints of the table being referenced; the only difference is that your FK attribute(s) can be NULL (whereas the referenced attribute(s) cannot).
