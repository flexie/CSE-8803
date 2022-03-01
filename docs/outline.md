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

### Recordings

- [Recording for Lecture 1](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220111_135930-Meeting%20Recording.mp4?csf=1&web=1&e=iVhGLL)

- [Recording for Lecture 2](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220113_135959-Meeting%20Recording.mp4?csf=1&web=1&e=If085B)

- [Recording for Lecture 3](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220118_135748-Meeting%20Recording.mp4?csf=1&web=1&e=UydDQV)

- [Recording for Lecture 5](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220125_135818-Meeting%20Recording.mp4?csf=1&web=1&e=Ce6ANU)
 
- [Recording for Lecture 6](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220127_135912-Meeting%20Recording.mp4?csf=1&web=1&e=aqTBsJ)

- [Recording for Lecture 7](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220201_135838-Meeting%20Recording.mp4?csf=1&web=1&e=ujaR71)

- [Recording for Lecture 8](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/New%20channel%20meeting-20220203_135918-Meeting%20Recording.mp4?csf=1&web=1&e=RKoFI9)

- [Recording for Lecture 9](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220208_135827-Meeting%20Recording.mp4?csf=1&web=1&e=TOlmLs)
 
- [Recording for Lecture 10](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220210_135810-Meeting%20Recording.mp4?csf=1&web=1&e=YbhclO)

- [Recording for Lecture 11](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220215_135810-Meeting%20Recording.mp4?csf=1&web=1&e=rzl0Ss)

- [Recording for Lecture 12](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220217_135851-Meeting%20Recording.mp4?csf=1&web=1&e=AwI09f)


- [Recording for Lecture 13](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220222_135840-Meeting%20Recording.mp4?csf=1&web=1&e=ga2CdN)

- [Recording for Lecture 13](https://gtvault.sharepoint.com/:v:/r/sites/Imagingwdata-drivenmodelsCSE8803/Shared%20Documents/General/Recordings/Meeting%20in%20_General_-20220224_142353-Meeting%20Recording.mp4?csf=1&web=1&e=VUAhpR)

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

### Bayesian Inference

### Reading material

- [Deep Bayesian inference for seismic imaging with tasks](https://slim.gatech.edu/content/deep-bayesian-inference-seismic-imaging-tasks)

### Slides

[Slide deck 1](https://www.dropbox.com/s/7dl3n8hmfnvmwed/11-ML-seismic-inverse.pdf?dl=0)

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

#### Untrained Neural Networks
- [Deep Image Prior](https://arxiv.org/pdf/1711.10925.pdf)
- [A Bayesian Perspective on the Deep Image Prior](https://arxiv.org/pdf/1904.07457.pdf)
- [DeepRED: Deep Image Prior Powered by RED](https://arxiv.org/pdf/1903.10176.pdf)
- [Algorithmic Guarantees for Inverse Imaging with Untrained Network Priors](https://arxiv.org/pdf/1906.08763.pdf)

#### Loop-Unrolled Neural Networks
- [Learning to learn by gradient descent by gradient descent]( https://arxiv.org/pdf/1606.04474.pdf )
- [Invert to Learn to Invert](https://papers.nips.cc/paper/8336-invert-to-learn-to-invert.pdf)
- [Recurrent Inference Machines for Solving Inverse Problems](https://www.ics.uci.edu/~welling/publications/papers/Submitted2016-RIM.pdf)
- [Model based learning for accelerated, limited-view 3D photoacoustic tomography](https://arxiv.org/pdf/1708.09832.pdf)
- [Multi-Scale Learned Iterative Reconstruction](https://arxiv.org/pdf/1908.00936.pdf)
- [Learned primal-dual reconstruction](https://arxiv.org/pdf/1707.06474.pdf)
- [Deep bayesian inversion](https://arxiv.org/pdf/1811.05910.pdf)
- [Solving ill-posed inverse problems using iterative deep neural networks](https://arxiv.org/pdf/1704.04058.pdf)
- [Low Shot Learning with Untrained Neural Networks for Imaging Inverse Problems](https://arxiv.org/abs/1910.10797)

#### Normalizing Flows

- First Papers
	- [NICE: NON-LINEAR INDEPENDENT COMPONENTS ESTIMATION  (2015)](https://arxiv.org/pdf/1410.8516.pdf)
	- [Variational Inference with Normalizing Flows (2016)](https://arxiv.org/pdf/1505.05770.pdf)
	- [DENSITY ESTIMATION USING REAL NVP (2017)](https://arxiv.org/pdf/1605.08803.pdf)
	- [Glow: Generative Flow with Invertible 1×1 Convolutions (2018)]( https://arxiv.org/pdf/1807.03039.pdf )

- Conditional Normalizing Flows
	- [HINT: Hierarchical Invertible Neural Transport for General and Sequential Bayesian inference](https://arxiv.org/pdf/1905.10687.pdf)
	- [GUIDED IMAGE GENERATION WITH CONDITIONAL INVERTIBLE NEURAL NETWORKS](https://arxiv.org/pdf/1907.02392.pdf)
	- [LEARNING LIKELIHOODS WITH CONDITIONAL NORMALIZING FLOWS](https://arxiv.org/pdf/1912.00042.pdf )

- Continuous Normalizing Flows
	- [Neural Ordinary Differential Equations](https://papers.nips.cc/paper/7892-neural-ordinary-differential-equations.pdf)
	- [FFJORD: FREE-FORM CONTINUOUS DYNAMICS FOR SCALABLE REVERSIBLE GENERATIVE MODELS]( https://arxiv.org/pdf/1810.01367.pdf )

- Applications
	- [Invertible generative models for inverse problems: mitigating representation error and dataset bias]( https://arxiv.org/pdf/1905.11672.pdf )
	- [Analyzing Inverse Problems with Invertible Neural Networks](https://arxiv.org/pdf/1808.04730.pdf)
	- [Compressible Latent-Space Invertible Networks for Generative Model-Constrained Image Reconstruction](https://arxiv.org/pdf/2007.02462.pdf )

- Review papers
	- [Normalizing Flows: An Introduction and Review of Current Methods](https://arxiv.org/pdf/1908.09257.pdf )
	- [Normalizing Flows for Probabilistic Modeling and Inference](https://arxiv.org/pdf/1912.02762.pdf)

- SOTA
	- [Flow++: Improving Flow-Based Generative Models with Variational Dequantization and Architecture Design](https://arxiv.org/pdf/1902.00275.pdf )
	- [Densely connected normalizing flows](https://arxiv.org/pdf/2106.04627.pdf )
	- [Neural Spline Flows](https://arxiv.org/pdf/1906.04032.pdf )
 
#### Diffusion Models (Equivalent to certain SDE models)
- [Denoising Diffusion Probabilistic Models](https://arxiv.org/pdf/2006.11239.pdf )
- [Diffusion Models Beat GANs on Image Synthesis](https://proceedings.neurips.cc/paper/2021/file/49ad23d1ec9fa4bd8d77d02681df5cfa-Paper.pdf )
- [Deblurring via Stochastic Refinement ](https://arxiv.org/pdf/2112.02475.pdf)

#### Stochastic Differential Equations Generative Models (Equivalent to certain Diffusion models)
- [Neural Ordinary Differential Equations](https://papers.nips.cc/paper/7892-neural-ordinary-differential-equations.pdf)
- [FFJORD: FREE-FORM CONTINUOUS DYNAMICS FOR SCALABLE REVERSIBLE GENERATIVE MODELS]( https://arxiv.org/pdf/1810.01367.pdf )
- [SCORE-BASED GENERATIVE MODELING THROUGH STOCHASTIC DIFFERENTIAL EQUATIONS](https://arxiv.org/pdf/2011.13456.pdf)
- [SOLVING INVERSE PROBLEMS IN MEDICAL IMAGING WITH SCORE-BASED GENERATIVE MODELS](https://arxiv.org/pdf/2111.08005.pdf)

#### GANs
- [Bayesian Inference with Generative Adversarial Network Priors](https://arxiv.org/pdf/1907.09987.pdf)
- [Deep Generative Adversarial Neural Networks for Compressive Sensing MRI](https://arxiv.org/pdf/1706.00051.pdf)
- [GAN-based Projector for Faster Recovery with Convergence Guarantees in Linear Inverse Problems](https://arxiv.org/pdf/1902.09698.pdf)
- [Solving Linear Inverse Problems Using GAN Priors: An Algorithm with Provable Guarantees](https://arxiv.org/abs/1802.08406)
- [Stochastic Seismic Waveform Inversion using Generative Adversarial Networks as a Geological Prior](https://arxiv.org/pdf/1806.03720.pdf)

#### Compressed Sensing
- [Learning-Based Compressive Subsampling](https://arxiv.org/pdf/1510.06188.pdf)
- [Learning-Based Compressive MRI](https://arxiv.org/pdf/1805.01266.pdf)
- [NETT Regularization for Compressed Sensing Photoacoustic Tomography](https://arxiv.org/pdf/1901.11158.pdf)

#### Misc
- [Stein Variational Gradient Descent: A General Purpose Bayesian Inference Algorithm]( https://arxiv.org/pdf/1608.04471.pdf )
- [Divergence Triangle for Joint Training of Generator Model, Energy-based Model, and Inference Model](https://arxiv.org/pdf/1812.10907.pdf)
- [Transport map accelerated Markov chain Monte Carlo](https://arxiv.org/pdf/1412.5492.pdf)
- [A transport-based multifidelity preconditioner for Markov chain Monte Carlo](https://arxiv.org/pdf/1808.09379.pdf)
- [Uncertainty Quantification with Generative Models](https://arxiv.org/pdf/1910.10046.pdf)
- [Variational Inference for Computational Imaging Inverse Problems](https://arxiv.org/pdf/1904.06264v2.pdf)
- [Adversarial Uncertainty Quantification in Physics-Informed Neural Networks](https://arxiv.org/pdf/1811.04026.pdf)





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