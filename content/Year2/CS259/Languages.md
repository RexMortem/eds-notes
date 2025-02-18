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

>[!Note]- Kleene Star
>The asterisk in $\Sigma^{*}$ is called the "Kleene Star".
>
>It is defined by $A^{*} = \{x_{1}x_{2} \dots x_{k} \; | \; k \geq 0, \; x_{i} \in A \}.$
>
>***Example 1:*** $\{0\}^{*} = \{\epsilon, 0, 00, 000, \dots\}.$
>***Example 2:*** $\{0,1\}^{*} = \{\epsilon, 0, 1, 00, 01, 10, 11, \dots\}.$


**Language** - a subset of all strings. $L \subseteq \Sigma^{*}$
