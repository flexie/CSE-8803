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

Chapter 2 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Fourier Transforms] from [Mathematical Foundations of Data Sciences].

[Fourier Transforms]:https://mathematical-tours.github.io/book-sources/chapters-pdf/fourier.pdf
[Mathematical Foundations of Data Sciences]:https://mathematical-tours.github.io/book/
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
Chapter 3 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Wavelets] from [Mathematical Foundations of Data Sciences].

[Wavelets]:https://mathematical-tours.github.io/book/

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
Chapter 4 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Linear and Non-linear Approximation] from [Mathematical Foundations of Data Sciences].

[Linear and Non-linear Approximation]:https://mathematical-tours.github.io/book-sources/chapters-pdf/approximation.pdf
###Assignments

See [assignment](homework.md) tab.

### Slides
[Approximation and Coding with Orthogonal Decompositions] adapted from [here].

[Approximation and Coding with Orthogonal Decompositions]:https://www.dropbox.com/s/2wa1nwecas2pykj/4-course-signal-approximation.pdf?dl=0

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
Chapter 5 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Denoising] from [Mathematical Foundations of Data Sciences].

[Denoising]:https://mathematical-tours.github.io/book-sources/chapters-pdf/denoising.pdf

### Assignments
See [assignment](homework.md) tab.

### Slides
[Linear and nonlinear denoising] adapted from [here].

[Linear and nonlinear denoising]:https://www.dropbox.com/s/xhpr4a4e60v7c9k/5-course-signal-denoising-new.pdf?dl=0
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
Chapter 6 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Variational Priors and Regularization] from [Mathematical Foundations of Data Sciences].

[Variational Priors and Regularization]:https://mathematical-tours.github.io/book-sources/chapters-pdf/variational-priors.pdf

### Assignments
See [assignment](homework.md) tab.

### Slides
[Inverse problems Regularization] adapted from [here].

[Inverse problems Regularization]:https://www.dropbox.com/s/let9p1m16hyiqzj/6-course-signal-inverse-pbm-variational-new.pdf?dl=0
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
Chapter 7 from [Advanced Signal, Image and Surface Processing]. If you want more detail read [Inverse Problems] and [Sparse Regularization] from [Mathematical Foundations of Data Sciences].

[Inverse Problems]:https://mathematical-tours.github.io/book-sources/chapters-pdf/inverse-problems.pdf
[Sparse Regularization]:https://mathematical-tours.github.io/book-sources/chapters-pdf/sparse-regularization.pdf
Assignments
See [assignment](homework.md) tab.

### Slides
[Sparse regularization of Inverse Problems] adapted from [here].

[Sparse regularization of Inverse Problems]:https://www.dropbox.com/s/idl446ja701xloe/7-course-signal-inverse-pbm-sparse-new.pdf?dl=0

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

### Reading material
[Compressive Sensing Chapter] from [Mathematical Foundations of Data Sciences].

[Compressive Sensing Chapter]:https://mathematical-tours.github.io/book-sources/chapters-pdf/compressed-sensing.pdf
### Slides
[Compressive Sensing] adapted from [here].

[Compressive Sensing]:https://www.dropbox.com/s/r4vs627jdyqfcnj/8-course-signal-compressive-sensing-new.pdf?dl=0

*** 

### General information generative neural networks

#### Slides on generative models

- [Tutorial on Deep Generative Models by DeepMind](https://www.shakirm.com/slides/DeepGenModelsTutorial.pdf)

- [Probabilistic Deep Learning by Microsoft](https://www.microsoft.com/en-us/research/uploads/prod/2018/03/Nowozin-Deep-Generative-Models-60-Minutes.pdf)

- [Lecture on Learning Deep Generative Models by Russ Salakhutdinov](http://www.cs.toronto.edu/~rsalakhu/Lecture1.pdf)
​
#### Ingredients of convolutional neural networks

- [Lecture on Convolutional Networks by Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/slides/lec11.pdf)
​
#### Tutorials and codes

-  [Super simple implementations of generative models in PyTorch and TensorFlow](https://github.com/wiseodd/generative-models) along with related [blog posts](https://wiseodd.github.io/)
​
-  [Collection of generative models in PyTorch](https://github.com/znxlwm/pytorch-generative-model-collections)
​
-  [Collection of generative models in TensorFlow](https://github.com/hwalsuklee/tensorflow-generative-model-collections)
​
​
#### Useful other material

- [Intro to Neural Networks and Machine Learning course - Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/)
​
- [Neural Networks and Deep Learning course - Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/)


### Statistical Regularization 

### Learning in Functional Analytic Regularization

### Learning in Statistical Regularization

[here]:https://mathematical-tours.github.io/slides/
[assignment]: