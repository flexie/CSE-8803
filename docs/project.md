# Class projects

## Data and scripts

The data required for the project is in the Dropbox folder used for the assignments

The projects are wrapped up in a docker image so that all the required dependencies are already installed. You will need to have docker installed. Once done run the following command

```
docker run -p 8888:8888 -v /path/to/files:/app/judi/data philippwitte/judi_eas_project:v1.0
```

where `/path/to/files` is the absolute location of the project data on your own machine. Running this command will produce an output that looks like

```
    
    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://(9d81a99a7494 or 127.0.0.1):8888/?token=7b1629792186c4e469d30eb92e8e9670d4f3bfa96c0c799f
```

Copy paste the URL in your browser and replace `(9d81a99a7494 or 127.0.0.1)` by `localhost`.

You will then be directed to a jupyter folder that contains the notebooks for the projects.

## Projects

As part of Lab 8, we are asking the students to work on a project in four groups. The projects are on the use of compressive sensing in seismic data acquisition and processing, and we are asking the students to make a comparison between different interpolation and acquisition techniques, namely

- missing trace interpolation via sparsity promoting techniques

- missing trace interpolation via rank minimization techniques

- acquisition with simultaneous randomly amplitude weighted sources or phase encoded sources for 'land’

Details on these different acquisition schemes will be discussed in class and during Lab 8. The goal of the project is to extend the 2D examples on common-receiver gathers to processing of a complete seismic line (for many receivers). This leads to a large problem with an unknown vector for which we need to invert with about 1 billion variables. As you do not have access to necessary resources you will need to solve the problem for each shot record or frequency slice independently and put the results back together afterward.

Scientifically, the acquisition and interpolation projects will focus on

- defining and testing the sampling matrix that models seismic acquisition. Kronecker products will be used to extend the 2D implementations of the sampling operators for common-receiver gathers to seismic lines that can be represented as a 3D volume. Plots have to be made of the sampling artifacts in the source-receiver-time domain and in the midpoint-offset-time domain. Also a study should be made of the size of the artifacts in relation to the degree of subsampling. We also would like to see plots of rows of the sampling matrix.

- selection of the appropriate sparsifying transform using curvelets and our Kronecker product. We would like to see a plot of a couple of columns of the synthesis matrix.

- in case of rank minimization techniques, selecting an appropriate rank plays a crucial role. Extract low and high frequency slices from a given seismic line. Look into the decay of singular values in each case and select rank accordingly.

- recovery of the fully-sampled sequential shot data by sparse inversion or matrix completion using SPGl1. The quality of the recovery should be measured via the signal-to-noise ratio ${SNR}=-20log_{10}(\frac{|{f}-\hat{{f}}|_2}{|{f}|_2})$ with f the original data and $\hat{{f}}$ the recovered data. Plots should also be made of the convergence as a function of the number of iterations. We also would like to see a plot of the residue as a function of the one-norm (sparsity case) or nuclear norm (matrix completion case) of the solution. In case of rank minimization, for a fixed sub-sampling ratio, plot SNR as a function of rank.

Each group is asked to give a short seminar on their project in class for 20 minutes with 15 to 17 minutes for the presentation itself and the remaining time for questions. The students are asked to divide the topics of the seminar into two or three parts presented by two or three different students in the team. During the question period each of the students will be asked to answer questions. The seminar will be graded using the following seminar evaluation form.

Please refer to the main page of the course for the date of the projection presentation in class.

Papers that are relevant for the projects are:

	Gilles Hennenfent and Felix J. Herrmann. Simply denoise: wavefield reconstruction via jittered undersampling, Geophysics, vol. 73, p. V19-V28, 2008. In the paper, the authors explain how to use jitter sampling to optimize the recovery from random missing shots.

	Felix J. Herrmann Yogi Erlangga and Tim T. Y. Lin. Compressive simultaneous full-waveform simulation. Geophysics, vol. 74, p. A35, (2009). In this paper, the authors apply compressive sensing to speedup wavefield simulations by using randomly weighted simultaneous sources.

	Felix J. Herrmann. Randomized sampling and sparsity: getting more information from fewer samples. Geophysics 75, WB173 (2010); doi:10.1190/1.350614. In this paper, the basics of compressive sensing are explained for a geophysics audience followed by discussion of different sampling schemes. You can skip the case studies.

	Felix J. Herrmann, Michael P. Friedlander, Ozgur Yilmaz. Fighting the curse of dimensionality: compressive sensing in exploration seismology. In this paper, the authors give an overview of the application of compressive sensing to exploration seismology.

	Haneet Wason and Felix J. Herrmann. Only dither: efficient simultaneous marine acquisition. EAGE expanded abstract. 2012. In this expanded abstract, the authors describe the application of compressive sensing to simultaneous marine acquisition.

	Haneet Wason, Felix J. Herrmann. Time-jittered ocean bottom seismic acquisition. SEG expanded abstract. 2013. In this abstract, the author describe the application of time-jittered marine acquisition scheme.

	Aleksandr Y. Aravkin, Rajiv Kumar, Hassan Mansour, Ben Recht, Felix J. Herrmann. A robust SVD-free approach to matrix completion, with applications to interpolation of large scale data. arXiv submission. In this paper, the author explain how to use rank-minimization techniques to recover random missing shots.

	Rajiv Kumar, Aleksandr Y. Aravkin, Ernie Esser, Hassan Mansour and Felix J. Herrmann. SVD-free low-rank matrix factorization : wavefield reconstruction via jittered subsampling and reciprocity. EAGE expanded abstract. 2014. In this expanded abstract, author explain the use of jittered sampling to optimize rank minimization based missing trace interpolation techniques.