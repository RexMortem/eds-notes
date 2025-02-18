May be useful to refresh yourself on terms in [[Intro to Formal Languages]], such as the 'Kleene Star'.

## Regular Expression Rules 

Regular Expressions have some fundamental rules; I'll present the rules along with the effect it has on the language generated. 

- $L(R) = \{a\}$ if $R = a$ 
	- $L(R) = \{\epsilon\}$ if $R = \epsilon$
- $L(R) = \emptyset$ if $R = \emptyset$
- $L(R) = L(R_{1}) \cup L(R_{2})$ if $R = R_{1} + R_{2}$ 
- $L(R) = L(R_{1}) \cdot L(R_{2})$ if $R = R_{1} \cdot R_{2}$
- $L(R) = L(R_{1})^{*}$ if $R = R_{1}^{*}$

>[!Note]- Kleene Plus
>Note that while we only define a rule for Kleene Star (**\***), we can also use Kleene Plus (**+**) in writing Regular Expressions.
>
>You can think of $A^{+}$ as a shorthand for $A \cdot A^{*}$


>[!Warning]- Regular Expressions vs Regex
>The regular expressions we learn in theoretical CS (and this module) are different from regex, which has far more expressive power than the 6 rules (7 if you include Kleene Plus) we've defined. 
>
>In fact, many languages which have regex actually present a system which is more powerful than regular expressions i.e. can do things that regular expressions can't do.
>
>Therefore, it's risky to use Regex symbols in this module. However, it is useful to think about representing Regex operations with regular expressions:
>
>
| Regex | Meaning                                        | Regular Expression |
| ----- | ---------------------------------------------- | ------------------ |
| $a?$  | $a$ is optional i.e. 0 or 1 occurrences of $a$ | $(a + \epsilon)$   |
|       |                                                |                    |
|       |                                                |                    |



### Converting NFAs into Regex 

Note that since DFAs are essentially NFAs, you can use this same approach for DFAs.


>[!Tip]- Stuck with generating Regular Expressions
>Try writing a DFA or NFA for it first.
>
>Writing a DFA/NFA for it forces you to think very carefully about which symbols lead to which states which makes writing an edge-case-free construct a lot easier. 
>
>If you can't generate the regular expression after writing the DFA/NFA, then you can apply the algorithm to convert NFAs into regular expressions.