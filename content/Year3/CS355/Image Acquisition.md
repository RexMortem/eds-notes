
## Image Fundamentals 

- (Some) Light reflects off the scene, and hits the optical lens which focuses the light
- Passes colour filter
- Light enters the **imaging sensor** 

We'll go into depth on each of these points now.

### Imaging Sensor 

### Sampling

Sampling is the discretization of space (since the real world is continuous, but the digital is discrete).

#### Spatial Resolution
Grid spacing size determines **spatial resolution** (how detailed the digital image is)
	- denser grids -> more pixels, more detail 

#### Sampling in 1D

$comb(t) = \begin{cases} 1 & \exists n. \; t = nT \\ 0 & otherwise \end{cases}$

#### Quantization 
The discretization of intensity values. 

Quantization is a more general concept which means to go from a larger (usually continuous) set to a smaller finite set i.e. it just means discretization.


### Colour Filter Array (CFA)
Filters for the three primary colours. 

#### Bayer Patterns 
The CFA is composed of 3 filters which form the RGB mosaic.

>![Info]- Why double the green?
>The green filter has double the number of cells, because the human eye has double the number of green absorption cells. 
>
>So it is to mimic human physiology. 

#### CFA Interpolation
We then have to recover the complete RGB image from the Bayer Pattern array; we do this through interpolation.

##### Linear Interpolation
Refer to [[Interpolation|Data Analytics]]

##### Bilinear Interpolation
Given 4 pixels, we can interpolate between two pixels (to get $x$) and then between the other two pixels (to get $y$). 

#### Gamma Correction

#### Grayscale Image

**Lecture Question 1:** What is the storage for a 128x128 grayscale image which takes 16 different intensity levels?
***Answer:*** $128 \times 128 \times log_{2}(16) = 128 \times 128 \times 4 = 65536$ bits.
**Lecture Question 2:** Amount of storage for an RGB image of the same dimension?