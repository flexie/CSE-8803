## Overview: a Sparse Tour of Signal Processing

*** 

## Signal and Image Processing with Orthogonal Decompositions

- Continuous signals and images
- Orthogonal representations
   - decomposition
	 - energy conservation (Parseval)
	 - Fourier and wavelets
	 - 2D wavelet transform

- Linear and nonlinear approximations
	 - filtering
	 - thresholding
	 - compressibility and its relation to smoothness
	 
- Denoising and inverse problems
	 - signal model
	 - recovery by sparsity promotion

### Reading material
Chapter 1 from [Advanced Signal, Image and Surface Processing]

[Advanced Signal, Image and Surface Processing]:https://www.dropbox.com/s/5pd1nec1cf7e2b4/AdvancedSignalProcessingNew.pdf?dl=0

### Slides

[Signal and Image Decomposition in Orthogonal Bases] adapted from [here].

[Signal and Image Decomposition in Orthogonal Bases]:https://www.dropbox.com/s/efy6fghhip6y7ko/1-course-signal-orthobases-new.pdf?dl=0
*** 

## Fourier Processing

- Continuous/discrete Fourier basis
- Sampling
- 2D Fourier transform
- Fourier Approximation

### Reading material

Chapter 2 from [Advanced Signal, Image and Surface Processing]

[Advanced Signal, Image and Surface Processing]:https://www.dropbox.com/s/5pd1nec1cf7e2b4/AdvancedSignalProcessingNew.pdf?dl=0
### Assignments

See [assignment](homework.md) tab.

### Slides

[Fourier Processing] adapted from [here].

[Fourier Processing]:https://www.dropbox.com/s/kbezzvt4b7ggh1z/2-course-signal-fourier-new.pdf?dl=0

*** 
## Wavelet Processing

- 1D Multiresolutions
   - detail spaces
	 - Haar wavelets
- 1D Wavelet transform
	- computing wavelet coefficients
	- discrete wavelet coefficients
	- fast wavelet transform
	-inverse transform
- Filter banks
	- approximation filter
	- detail filter
	- vanishing moments
	- Daubechies wavelets
- Extension to 2D
	-anisotropic wavelets
	- 2D multiresolutions
	- 2D wavelet bases
	- 2D discrete wavelet coefficients
	- fast 2D wavelet transform

###Reading material
Chapter 3 from [Advanced Signal, Image and Surface Processing]


###Assignments
See [assignment](homework.md) tab.

### Slides

[Wavelet Processing] adapted from [here].

[Wavelet Processing]:https://www.dropbox.com/s/wudhbew83lamxfg/3-course-signal-wavelets-new.pdf?dl=0


***
## Approximation with Orthogonal Decompositions

- Linear and nonlinear approximations
	 - Sparse approximation in a basis
	 - hard thresholding
	 - decay of approximation errors (linear vs. nonlinear)
	 - Relation between decay rate coefficients and approximation error
	 - Fourier for smooth functions
	 - Fourier and singularities/edges
- wavelet transform for peice-wise 1D smooth functions
	- vanishing moments
	- magnitude of wavelet coefficients and its relation to edges
	- decay and nonlinear approximation error for piece-wise 1D functions
- Piece-wise smooth 2D functions
	- 2D approximations
	-decay and nonlinear approximation error for piece-wise 2D functions
- Geometrically regular functions
	- space of BV functions
	-	finite elements
	- curvelets, their construction, and properties

### Reading material
TBA

###Assignments

See [assignment](homework.md) tab.

### Slides
[Approximation and Coding with Orthogonal Decompositions] adapted from [here].

***

## Linear and Nonlinear Denoising

- Linear denoising
   - additative noise model
	 - linear denoising by smoothing
	 - Wiener filter and oracle estimation of optimal filter
- Nonlinear denoising
	- hard thresholding
	- optimal threshold selection
	-	nonlinear approximation and estimation
	- hard vs. soft thresholding
- Translational invariant thresholding
	- translation invariant wavelets
	- optimal threshold
- Other diagonal estimators
	- between hard and soft thresholding
- Non-diagonal estimators
	- block thresholding

### Reading material
TBA

### Assignments
See [assignment](homework.md) tab.

### Slides
[Linear and nonlinear denoising] adapted from [here].

***

## Variational Regularization of Inverse Problems

- Variational priors
   - smooth and cartoon
	 - natural image priors
	 - discretization
- Variational regularization
	- regularized inverse
	- pseudo inverse
	- Sobolev regularization and inpainting
	- total variation regularization and inpainting
- Example from tomography with the Radon transform

###Reading material
TBA

### Assignments
See [assignment](homework.md) tab.

### Slides
[Inverse problems Regularization] adapted from [here].

*** 

## Sparse Regularization of Inverse Problems

- Linear inverse problems
	- denoising
	- inpainting
	- super- resolution
- Regularization of inverse problems
	- regularized inverse
	- Lagrangian formulation including the the Lagrange multiplier/trade-off parameter lambda
	- smooth and cartoon priors
- Redundant dictionaries
- Sparse priors
	- convex relaxation of the $\ell_0-norm$ via the $\ell_1$-norm
	- $\ell_1$-regularization and sparse recovery
	- noise-free sparsity-promoting regularization
- Iterative soft thresholding

### Reading material
TBA

Assignments
See [assignment](homework.md) tab.

### Slides
[Sparse regularization of Inverse Problems] adapted from [here].

***


## Compressive Sensing

- Classical sampling
   - discretization
	 - point-wise sampling and smoothness
- Compressive acquisition
	- examples single pixel camera
	- physical model
- Inversion and sparsity
	- $\ell_1$ prior
	- sparse CS recovery
- Theoretical guarantees
	- CS with restricted isometry constants (RIP)
	- singular-value distributions
	- RIP for Gaussian matrices
	- numerics with RIP
- Fourier measurements
	- MRI imaging
	- radar interferometry
	- structured measurements

### Assignments
See [assignment](homework.md) tab.

### Slides
[Compressive Sensing] adapted from [here].

*** 
### Statistical Regularization 

### Learning in Functional Analytic Regularization

### Learning in Statistical Regularization

[here]:https://mathematical-tours.github.io/slides/
[assignment]: