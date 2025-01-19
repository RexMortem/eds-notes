**Interpolation** is estimating unknown values between known values. 
Generally, given data points, interpolation finds a smooth function that passes through all the data points. 

***Example:*** For the points (1,3) and (2,7), we can fit the function $y=4x - 1$. 
Now, we can provide values for x= 1.5, x = 1.32, x = 1.999 etc. 

## Practical Uses

- We can go from a low-res photo to a high-res photo by interpolating; we are estimating the colour values of the newly generated pixels! 
## Types of Interpolation 

- Linear Interpolation (lerp) - connects two points with a straight line 
- Polynomial Interpolation - a single polynomial connects all points 
	- Includes Lagrange, Newton interpolation techniques 
- Spline Interpolation - piecewise polynomials (avoids oscillations)

## Naive Polynomial Interpolation

For $n$ data points, we can generate a polynomial of degree $n-1$. This is an upper-bound for the degree that a polynomial must be to go through all the data points! 

***Example:*** Given data points (1,2), (3, 4), and (5,8). Give a polynomial interpolation

$y = a_{0}x^{2} + a_{1}x^{1} + a_{2}$.

Subbing in the points: 
$g$

### Vandermonde Matrix

### Generalised Theorem 

***Theorem:*** Given $n+1$ data points $(x_{0}, y_{0}), (x_{1}, y_{1}), \dots, (x_{n+1}, y_{n+1})$

### Horner Scheme

$a_{0} + a_{1}x + a_{2}x^{2} + \dots + a_{n}x^{n} = a_{0} + x(a_{1} + x(a_{2} + \dots))$

Derived from just factoring out the $x$ each time

### Limitations of Naive Polynomial Interpolation 

1) Finding the inverse of the Vandermonde matrix is expensive
2) No support for incremental update; have to recalculate the polynomial from scratch 
3) Must find the whole function first (determine coefficients) before finding estimates for intermediate points 

**Lagrange Interpolation** solves problems 1 and 3.
**Newton Interpolation** solves problems 2 and 3. 

## Lagrange Polynomial

### Divided Difference

1st order divided difference is the gradient/rate-of-change of the line between the two parts. 
2nd order divided difference is the rate of change of the 1st order divided differences.

$[y_{0}, y_{1}, \dots, y_{n-1}, y_{n}] = \frac{}{}$

***Example:*** Evaluate $[y_{0}, y_{1}, y_{2}]$ for $(x_{0}, y_{0}), (x_{1}, y_{1}), (x_{2}, y_{2})$

First, calculate the 1st order divided differences. 

$[y_{0}, y_{1}] = \frac{y_{1} - y_{0}}{x_{1} - x_{0}}$

#### Divided Difference Properties

**Property 1:** 
**Property 2:** 

#### Newton Interpolation 

*Exercise:* Inductive argument? 

***Example:*** Given points $(1,2), (3,4), (5,8)$, find a 2-degree Newton polynomial. 

$[y_{0}, y_{1}] = \frac{4-2}{3-1} = 2$. 
$[y_{1}, y_{2}] = \frac{8-5}{4-3} = 3$

$[y_{0}, y_{1}, y_{2}] = \frac{[y_{2}, y_{1}] - [y_{1}, y_{0}]}{x_{2} - x_{0}} = \frac{3-2}{4-1} = \frac{1}{3}$.