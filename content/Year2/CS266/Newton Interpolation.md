
*Exercise:* Inductive argument? 

***Example:*** Given points $(1,2), (3,4), (5,8)$, find a 2-degree Newton polynomial. 

$[y_{0}, y_{1}] = \frac{4-2}{3-1} = 2$. 
$[y_{1}, y_{2}] = \frac{8-5}{4-3} = 3$

$[y_{0}, y_{1}, y_{2}] = \frac{[y_{2}, y_{1}] - [y_{1}, y_{0}]}{x_{2} - x_{0}} = \frac{3-2}{4-1} = \frac{1}{3}$.

>[!Warning]- Runge Phenomenon
>Fitting a single high-degree polynomial to many data points can lead to erroneous oscillations; the solution is to use several piece-wise low-degree polynomials! 
>
