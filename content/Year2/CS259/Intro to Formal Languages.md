Sipser's *Introduction to the Theory of Computation (2nd Edition)* is very highly recommended.

We will discuss various models of computation.
## Basic Terminology 

**Alphabet** - a finite set (of symbols/letters). Examples include:
- $\{0, 1\}$
- $\{a,b,c, \dots, z\}$

We denote an alphabet by $\Sigma$
In this module, alphabets are finite

**String (word)** - a finite sequence of symbols. Examples include:
- $hello$ for $\Sigma = \{a,b,c,\dots,z\}$

$\Sigma^{*}$ means "all strings".
$\epsilon$ means "empty string".
$\Sigma^{+}$ means "all non-empty strings" i.e. $\Sigma^{+} = \Sigma^{*} \setminus \{\epsilon\}$

**Language** - a subset of all strings. $L \subseteq \Sigma^{*}$

