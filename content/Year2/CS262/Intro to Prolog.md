>![Note]- Fun Fact (about the name)
>The name 'Prolog' was chosen as an abbreviation of 'Programmation en logique', which is French for 'Programming in Logic'.
>
>So Prolog is short for 'Programming in Logic'. 

- Spaces/whitespace don't matter (?)
- Interpreter processes file from top to bottom
## Getting Started

### Loading Files 
```prolog
[fileName].
```

## Trace Mode

Use 
```prolog
trace
```
to activate trace mode.

Use 
```
notrace
```
to deactivate trace mode. 

## Atoms

Individual objects that can't be decomposed. Can be strings.

### Predicates
A type of atom with argument(s).


## Rules

***Example:*** 
```prolog
likes(Ed, Food) :- tasty(Food).
```

***Example 3:*** 
```prolog
likes(YoungEd, Food) :- likes(Ed, Food), notSpicy(Food).
```
## Unification

Can the interpreter unify the query with this line?

Thing must start with capital letter OR underscore symbol (test this?)

Use **;** to step through possible atoms that satisfy the predicate

## How do Imperative concepts map to Prolog?

#### if X AND Y 

Rule with multiple things. 

#### if X OR Y

Many rules. 
#### Assignment

is command 