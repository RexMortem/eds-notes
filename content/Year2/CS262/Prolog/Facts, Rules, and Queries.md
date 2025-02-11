Prolog programs are **knowledge bases (KBs)** which are a collection of facts and rules. 
Using the prolog program is then performing queries on that KB. 

## Querying 
If a fact is not written in the KB, or it cannot be inferred from the rules, then it is assumed to not be true. 

***Example:*** Does Ed play guitar? 

```prolog 
person(Ed).
person(Emily).
playsGuitar(Emily).
```
Asking: 
```prolog
?-playsGuitar(Ed). % should be 'no'
```

Since it is not written in the KB that 'Ed' plays guitar, it is assumed to be false. 

## Rules 

### F
```prolog
happy(ed):- hasVimto(ed).
```
*'ed' is happy given ed has vimto, or 'ed' is happy if ed has vimto*

>[!note]- modus ponens
>AAAAAAAAAAAAA

## Conjunction, Disjunction

You can express **conjunction** for a rule by having predicates next to each other, joined by a comma. 

***Example 1:*** 
```prolog
happy(ed):- noCoursework(ed), hasVimto(ed).
```
The above means *ed is happy* if *ed has no coursework* AND *ed has vimto*. So the comma serves as a conjunction operator. 

You can express **disjunction** for a rule by having multiple rules, or by using a semicolon. 
Let's have a look at multiple rules first.

***Example 2:*** 
```prolog 
happy(ed):- noCoursework(ed), hasVimto(ed).
happy(ed):- bigBagOfMoney(ed).
```
The above means that *ed is happy* if either of the following is true:
- *ed has no coursework* AND *ed has vimto*
- *ed has a big bag of money*

This could also be expressed in a single rule using '**;**' which is the disjunction operator. 

***Example 3:***
```prolog
happy(ed) :- 
	noCoursework(ed), hasVimto(ed);
	bigBagOfMoney(ed).
```

>[!Note]- Multiple Rules or Semicolon?
>Multiple Rules can be more readable than having many semicolons.
>
>Programs with semicolons may have a single rule where you would otherwise write many; therefore, it's a generally more efficient program since having a single rule will generally be faster. 

## Tutorial

### KB5

Definition lets people be jealous of themselves; could be better to add condition that $X,Y$ be distinct. 