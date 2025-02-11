
We get a more concise formula with additional constraints ->
- must be evenly spaced

## Equally Spaced Points 

$x_{i} = x_{0} + i \times h$ where $i = 0,1,2, \dots$
$x = x_{0} + t \times h$
$x - x_{i} = t \times h - i \times h$

### Forward Difference Operator 

$\Delta y_{i} = y_{i+1} - y_{i}$

$\Delta^{n} y_{i} = \Delta^{n-1}y_{i+1} - \Delta^{n-1}y_{i}$

### Forward Difference and Divided Difference

First order: $[y_{0}, y_{1}] = \frac{y_{1} - y_{0}}{x_{1} - x_{0}} = \frac{\Delta y_{0}}{h}$

Second order: $[y_{0}, y_{1}, y_{2}] = \frac{[y_{1}, y_{2}] - [y_{0}, y_{1}]}{x_{2} - x_[0]} = \frac{\frac{\Delta y_{1}}{h} - \frac{\Delta y_{0}}{h}}{2h}$

