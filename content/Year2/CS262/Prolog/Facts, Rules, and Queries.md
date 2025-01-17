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