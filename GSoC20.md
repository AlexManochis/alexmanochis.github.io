---
layout: page
title: Google Summer of Code 2020
---

## <span style="text-align:center;">Final Evaluation of my GSoC20 project  

### <span style="text-align:center;">Organization: GeomScale  
### <span style="text-align:center;">Project: A comparative study of uniform high dimensional samplers  
### <span style="text-align:center;">Topic:  Computational Statistics and Geometry  

#### *mentors:* Apostolos Chalkis, Vissarion Fisikopoulos, Elias Tsigaridas  
#### *Student:* Alex Manochis

You can read the proposal I submitted in Student application period [here](https://drive.google.com/file/d/1HiUnzKwEE5-PIVtFyS9TvHrgh3wUH5PN/view?usp=sharing)

#### Abstract

Uniform sampling from convex polytopes in high dimensions is very useful in many scientific fields and applications. The package `volesti` is a `C++` software with an R interface in `cran` which provides 4 geometric random walks for uniform sampling from convex polytopes and three state-of-the-art algorithms for volume approximation being the first package providing such a variety of 
options in geometric statistics. However, it is difficult to know when the Markov chain converges to the target distribution in order to stop sampling. MCMC Diagnostics are tools that can be used to check whether the quality of a sample generated with an MCMC algorithm is sufficient to provide an accurate approximation of the target distribution. The goals of this project were to provide: i) diagnostic tools for a random walk to check convergence to the target distribution, ii) efficient implementations of all the known geometric random walks for uniform sampling from convex bodies, that are not implemented in `volesti` and iii) an improved implementation for Billiard walk which is already implemented in `volesti`. The diagnostic tools would allow us to compare the mixing time of various random walks, which is a classical and hard problem in high dimensional statistics. Finally, it is my belief that these implementations will provide open source implementations to perform computations that are intractable till now in applications that require uniform sampling in high dimensions such as in computation biology (in thousands of dimensions) and multivariate integration (hundreds of dimensions). 

### My deliverables    

I have completed all the goals of the coding project. Moreover, I have provided package `volesti` with several additional C++ implementations for high dimensional sampling, rounding convex polytopes and MCMC diagnostics. In particular, my deliverables consist of the following C++ implementations and the corresponding R interfaces:  

- Accelarated version of Billiard Walk and faster volume estimation for H-polytopes.  
- Dikin Walk (based on the software [here](https://github.com/rzrsk/vaidya-walk)).  
- Vaidya Walk (based on the software [here](https://github.com/rzrsk/vaidya-walk)).  
- John Walk (based on the software [here](https://github.com/rzrsk/vaidya-walk)).  
- Multivariate PSRF Diagnostic of S. Brooks and A. Gelman.  
- Multivariate Geweke's MCMC Diagnostic.  
- Raftery's and Lewis' MCMC Diagnostic.  
  
My extra deliverables consist the following C++ implementations and the corresponding R interfaces:  

- Univariate interval PSRF Diagnostic of S. Brooks and A. Gelman.  
- Univariate PSRF Diagnostic of D.B. Rubin and A. Gelman.  
- A rounding method based on the computation of the maximum inscribed ellipsoid for H-polytopes.  
- A rounding method based on the isotropic position of a uniform sample from a polytope (it works for all the polytope representations).  
- Sampling and volume estimation for low dimensional polytopes.  

My PRs are the followings:  

1. [Accelerated billiard walk](https://github.com/GeomScale/volume_approximation/pull/92)  
2. [Dikin, Vaidya, John walk](https://github.com/GeomScale/volume_approximation/pull/88)  
3. [Adding two rounding methods](https://github.com/GeomScale/volume_approximation/pull/96)  
4. [MCMC diagnostics](https://github.com/GeomScale/volume_approximation/pull/106)  
5. [Marginal diagnostics and optimizations](https://github.com/GeomScale/volume_approximation/pull/108)  




