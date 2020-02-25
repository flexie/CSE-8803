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


### Statistical Regularization 

The review article [Solving inverse problems using data-driven models] serves as the major reading material. For a mathematical description of the February 6 and 11 lectures, refer to pages 22 till 43 from this article. 

### Learning in Functional Analytic Regularization

During the lecture of February 13, we start by considering section 5.1.2 Deep direct Bayes estimation on page 84 of [Solving inverse problems using data-driven models] untile Regularization by learning. We continue with section Deep direct estimation of higher-order moments on page 99. Next, we consider loop unrolling described in section 4.9 Data-driven optimization on page 66 until section 4.10 and later in section 5.1.4 Learned iterative schemes on page 89 until section 5.1.5. The supervised training, learned prior/regularizer, unsupervised learning, and semi-supervised learning are briefly introduced in section 5.1 Learning an estimator on page 82. 

### Learning in Statistical Regularization

[Solving inverse problems using data-driven models]:https://www.cambridge.org/core/journals/acta-numerica/article/solving-inverse-problems-using-datadriven-models/CE5B3725869AEAF46E04874115B0AB15

### Slides

We use a combination of slides developed mainly by Ozan Oktem and [Jonas Adler](https://jonasadler.com) and others. The slides presented in class can be found [here](https://www.dropbox.com/s/j6b5d0njmb7hzsj/Oktem.pdf?dl=0). 

***

### Papers

- [Learning-Based Compressive Subsampling](https://arxiv.org/pdf/1510.06188.pdf)

- [MoDL: Model Based Deep Learning Architecture for Inverse Problems](https://arxiv.org/pdf/1712.02862.pdf)

- [Learning-Based Compressive MRI](https://arxiv.org/pdf/1805.01266.pdf)

- [NETT Regularization for Compressed Sensing Photoacoustic Tomography](https://arxiv.org/pdf/1901.11158.pdf)

- [Divergence Triangle for Joint Training of Generator Model, Energy-based Model, and Inference Model](https://arxiv.org/pdf/1812.10907.pdf)

- [A Stein variational Newton method](https://papers.nips.cc/paper/8130-a-stein-variational-newton-method.pdf)

- [Neural Ordinary Differential Equations](https://papers.nips.cc/paper/7892-neural-ordinary-differential-equations.pdf)

- [Invert to Learn to Invert](https://papers.nips.cc/paper/8336-invert-to-learn-to-invert.pdf)

- [Recurrent Inference Machines for Solving Inverse Problems](https://www.ics.uci.edu/~welling/publications/papers/Submitted2016-RIM.pdf)

- [Model based learning for accelerated, limited-view 3D photoacoustic tomography](https://arxiv.org/pdf/1708.09832.pdf)

- [Multi-Scale Learned Iterative Reconstruction](https://arxiv.org/pdf/1908.00936.pdf)


- [Sensitivity of a partially learned model-based reconstruction algorithm](https://ris.utwente.nl/ws/portalfiles/portal/103725020/Boink_et_al._2018_Sensitivity_of_a_partially_learned_model_based_reconstruction_algorithm.pdf)

- [Degrees of Freedom Analysis of Unrolled Neural Networks](https://arxiv.org/pdf/1906.03742.pdf)

- [Deep Generative Adversarial Neural Networks for Compressive Sensing MRI](https://arxiv.org/pdf/1706.00051.pdf)

- [Solving ill-posed inverse problems using iterative deep neural networks](https://arxiv.org/pdf/1704.04058.pdf)

- [Learned primal-dual reconstruction](https://arxiv.org/pdf/1707.06474.pdf)

- [Learning to solve inverse problems using Wasserstein loss](https://arxiv.org/pdf/1710.10898.pdf)

- [Deep bayesian inversion](https://arxiv.org/pdf/1811.05910.pdf)

- [Transport map accelerated Markov chain Monte Carlo](https://arxiv.org/pdf/1412.5492.pdf)

- [A transport-based multifidelity preconditioner for Markov chain Monte Carlo](https://arxiv.org/pdf/1808.09379.pdf)

- [Guided Image Generation with Conditional Invertible Neural Networks](https://arxiv.org/pdf/1907.02392.pdf)

- [GAN-based Projector for Faster Recovery with Convergence Guarantees in Linear Inverse Problems](https://arxiv.org/pdf/1902.09698.pdf)

- [Solving Linear Inverse Problems Using GAN Priors: An Algorithm with Provable Guarantees](https://arxiv.org/abs/1802.08406)

- [Low Shot Learning with Untrained Neural Networks for Imaging Inverse Problems](https://arxiv.org/abs/1910.10797)

- [Stochastic Seismic Waveform Inversion using Generative Adversarial Networks as a Geological Prior](https://arxiv.org/pdf/1806.03720.pdf)

- [Uncertainty Quantification with Generative Models](https://arxiv.org/pdf/1910.10046.pdf)

- [Bayesian Inference with Generative Adversarial Network Priors](https://arxiv.org/pdf/1907.09987.pdf)

- [A Bayesian Perspective on the Deep Image Prior](https://arxiv.org/pdf/1904.07457.pdf)

- [Variational Inference for Computational Imaging Inverse Problems](https://arxiv.org/pdf/1904.06264v2.pdf)

- [DeepRED: Deep Image Prior Powered by RED](https://arxiv.org/pdf/1903.10176.pdf)

- [Algorithmic Guarantees for Inverse Imaging with Untrained Network Priors](https://arxiv.org/pdf/1906.08763.pdf)

- [Adversarial Uncertainty Quantification in Physics-Informed Neural Networks](https://arxiv.org/pdf/1811.04026.pdf)

- [HINT: Hierarchical Invertible Neural Transport for General and Sequential Bayesian inference](https://arxiv.org/pdf/1905.10687.pdf)

- [Analyzing Inverse Problems with Invertible Neural Networks](https://arxiv.org/pdf/1808.04730.pdf)


*** 

### General information generative neural networks

#### Slides on generative models

- [Lecture on Deep Generative Models by Joe Marino](http://www.yisongyue.com/courses/cs155/2019_winter/lectures/Lecture_16.pdf) - [Video](https://www.youtube.com/watch?v=Sb6RQfG-QQM)

- [Tutorial on Deep Generative Models by DeepMind](https://www.shakirm.com/slides/DeepGenModelsTutorial.pdf)

- [Probabilistic Deep Learning by Microsoft](https://www.microsoft.com/en-us/research/uploads/prod/2018/03/Nowozin-Deep-Generative-Models-60-Minutes.pdf)

- [Lecture on Learning Deep Generative Models by Russ Salakhutdinov](http://www.cs.toronto.edu/~rsalakhu/Lecture1.pdf)

#### Ingredients of convolutional neural networks

- [Lecture on Convolutional Networks by Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/slides/lec11.pdf)

- [Lecture on Convolutional Networks by Fei-Fei Li](http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture5.pdf)

- Lectures ([Part 1](https://github.com/rasbt/stat479-deep-learning-ss19/blob/master/L13_intro-cnn/L13_intro-cnn-part1_slides.pdf), [Part 2](https://github.com/rasbt/stat479-deep-learning-ss19/blob/master/L13_intro-cnn/L13_intro-cnn-part2_slides.pdf), [Part 3](https://github.com/rasbt/stat479-deep-learning-ss19/blob/master/L13_intro-cnn/L13_intro-cnn-part3_slides.pdf)) on Convolutional Neural Networks by Sebastian Raschka

- [Visual guide to convolution arithmetic in the context of deep learning](https://github.com/vdumoulin/conv_arithmetic), and [associated paper](https://arxiv.org/pdf/1603.07285.pdf)

#### Tutorials and codes

- [GAN lab, an interactive visualization for playing with GANs](https://poloclub.github.io/ganlab/)

- [A collection of various deep learning architectures, in TensorFlow and PyTorch (Jupyter Notebooks), by Sebastian Raschka](https://github.com/rasbt/deeplearning-models)

- [Super simple implementations of generative models in PyTorch and TensorFlow](https://github.com/wiseodd/generative-models) along with related [blog posts](https://wiseodd.github.io/)

- [Collection of generative models in PyTorch](https://github.com/znxlwm/pytorch-generative-model-collections)

- [Collection of generative models in TensorFlow](https://github.com/hwalsuklee/tensorflow-generative-model-collections)

#### Useful other material

- [Deep Learning course - Sebastian Raschka](http://pages.stat.wisc.edu/~sraschka/teaching/stat479-ss2019/)

- [Machine Learning & Data Mining course by Yisong Yue](http://www.yisongyue.com/courses/cs155/2019_winter/)

- [Introduction to Deep Learning and Generative Models course - Sebastian Raschka (Spring 2020)](http://pages.stat.wisc.edu/~sraschka/teaching/stat453-ss2020/)

- [Intro to Neural Networks and Machine Learning course - Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/)

- [Neural Networks and Deep Learning course - Roger Grosse](http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/)

- [Inverse Problems and Learning course - Ivan Dokmanic](https://courses.engr.illinois.edu/ece598id/sp2019/)

- [Troubling Trends in Machine Learning Scholarship](https://arxiv.org/abs/1807.03341)

[here]:https://mathematical-tours.github.io/slides/
[assignment]: