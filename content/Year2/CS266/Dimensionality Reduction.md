
The curse of dimensionality. 

**Dimensionality Reduction** is reducing the "dimension" of the data set. In time series analysis, the dimension is the number of data points. 

## PAA

Reduce the number of points by taking the average value for each segment. Given $X$ points, we want $N$ segments -> Reduced PAA -> Reconstructed PAA.

Length of each segment = $\frac{X}{N}$. 

***Example 1:*** 

### Limitations

## APCA

An adaptive PAA; it is called adapative, because it allows segments to be of variable lengths. 
### Haar Discrete Wavelet Transform (DWT)

- Find DWT Coefficients
- Truncate DWT Coefficients
- Reconstruct DWT
- Truncate if padded
- Replace approximates with actual averages

If mismatch in desired segments and achieved segments:
- will have to merge segments
	- we merge adjacent segments with least deviation in value 
	- merging is averaging 
	- repeat this process until desired segments = achieved segments 
***Example:*** $C=\{4.5, 0.5, 1, -1, 1, 1, -1, 1\}$

$4.5 + 0.5 = 5$ 
$4.5 - 0.5 = 4$
---

$5 + 1 = 6$
$5 - 1 = 4$

$4 + -1 = 3$
$4 - -1 = 5$

---
$6 + 1 = 7$
$6 - 1 = 5$

$f$
---

