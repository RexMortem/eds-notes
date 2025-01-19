We introduce some notation for modular arithmetic, and then some basic rules that'll help us solve some modular arithmetic problems. 

## Notation

We introduce $a \overset{b}{\equiv} c$ to mean that the remainder of $a \div b$ is $c$. Therefore, we have that $a = xb + c$ where $x \in \mathbb{Z}$. 

## Rules

***Multiplication Rule:*** we can multiply both sides of $a \overset{b}{\equiv} c$ to get $az \overset{b}{\equiv} cz$. 
**Proof:** $a \overset{b}{\equiv} c$ means $a = xb + c$. 

$za = zxb + zc$. 
$za = zxb + zc \overset{b}{\equiv} zc$. since $zxb$ is divisible by $b$. 

***Example:*** $10^{1} \overset{9}{\equiv} 1$. Applying the rule, $10^{2} \overset{9}{\equiv} 10$. 
In this case, we get that $cz > b$, so we'll have to apply $\overset{9}{\equiv}$ again.
$10^{2} \overset{9}{\equiv} 10 \overset{9}{\equiv} 1$.


## Modular Arithmetic Problems
***Example 1:*** $10^{100} \overset{7}{\equiv} x$. What is $x$?

>[!Check]- Solution
>$10^{1} \overset{7}{\equiv} 3$
>$10^{2} \overset{7}{\equiv} 30 \overset{7}{\equiv} 2$
>$10^{3} \overset{7}{\equiv} 20 \overset{7}{\equiv} 6$
>$10^{4} \overset{7}{\equiv} 60 \overset{7}{\equiv} 4$
>$10^{5} \overset{7}{\equiv} 40 \overset{7}{\equiv} 5$
>$10^{6} \overset{7}{\equiv} 50 \overset{7}{\equiv} 1$
>$10^{7} \overset{7}{\equiv} 10 \overset{7}{\equiv} 3$
>
>We've encountered a "loop" since $10^{1}$ has the same remainder as $10^{7}$. So if you apply 6 steps then it resets; $10^{1} \overset{7}{\equiv} 10^{7} \overset{7}{\equiv} 10^{13} \overset{7}{\equiv} \dots$ and so on. 
>
>Hence $10^{100} = 10^{96} \times 10^{4} \overset{7}{\equiv} 10^{4} \overset{7}{\equiv} 4$. So $x = 4$. 


***Example 2:*** (Follow-up to Example 1). $10^{10^{10}} \overset{7}{\equiv} x$. What is $x$?

>[!Check]- Solution
>Following on from ***Example 1***, we know that $10^{x} \overset{7}{\equiv} 10^{x+6}$ and further that $10^{x} \overset{7}{\equiv} 10^{x + 6y}$ where $y \in \mathbb{N}$. 
>
>If we can find out what the exponent (which is $10^{10}$) mod 6 is, then we can find out $x$. For instance, if $10^{10} \overset{6}{\equiv} r$ then we know $10^{10} = 6a + r$ where $a \in \mathbb{Z}$. So then we'll know $10^{10^{10}} = 10^{6a} \times 10^{r} \overset{7}{\equiv} 10^{r}$.
>
>$10^{1} \overset{6}{\equiv} 4$
>$10^{2} \overset{6}{\equiv} 40 \overset{6}{\equiv} 4$
>
>Okay so we know the remainder modulo 6 of any $10^{n}$ is going to be 4. So we know $10^{10^{10}} = 10^{6a} \times 10^{4} \overset{7}{\equiv} 10^{4} \overset{7}{\equiv} 4$. So $x=4$.
>
 