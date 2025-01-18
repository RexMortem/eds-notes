***Example:*** $10^{100} \overset{7}{\equiv} x$. What is $x$?

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