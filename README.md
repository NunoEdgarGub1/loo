[<img src="https://raw.githubusercontent.com/stan-dev/logos/master/logo_tm.png" width=100 alt="Stan Logo"/>](http://mc-stan.org)

# loo

[![Travis-CI Build Status](https://travis-ci.org/stan-dev/loo.svg?branch=master)](https://travis-ci.org/stan-dev/loo)
[![codecov](https://codecov.io/gh/stan-dev/loo/branch/master/graph/badge.svg)](https://codecov.io/github/stan-dev/loo?branch=master)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/loo?color=blue)](http://cran.r-project.org/web/packages/loo)
[![RStudio_CRAN_mirror_downloads_badge](http://cranlogs.r-pkg.org/badges/grand-total/loo?color=blue)](http://cran.r-project.org/web/packages/loo)

### Efficient approximate leave-one-out cross-validation for fitted Bayesian models

Leave-one-out cross-validation (LOO) and the widely applicable information
criterion (WAIC) are methods for estimating pointwise out-of-sample
prediction accuracy from a fitted Bayesian model using the log-likelihood
evaluated at the posterior simulations of the parameter values. LOO and WAIC
have various advantages over simpler estimates of predictive error such as
AIC and DIC but are less used in practice because they involve additional
computational steps.

The __loo__ R package package implements the fast and stable computations 
for LOO and WAIC from

* Vehtari, A., Gelman, A., and Gabry, J. (2017). Practical Bayesian model 
evaluation using leave-one-out cross-validation and WAIC. 
_Statistics and Computing_. 27(5), 1413--1432. 
doi:10.1007/s11222-016-9696-4. [Online](http://link.springer.com/article/10.1007\%2Fs11222-016-9696-4), 
[arXiv preprint arXiv:1507.04544](http://arxiv.org/abs/1507.04544).

* Vehtari, A., Gelman, A., and Gabry, J. (2017). Pareto smoothed importance sampling. 
[arXiv preprint arXiv:1507.02646](http://arxiv.org/abs/1507.02646).

From existing posterior simulation draws, we compute LOO using Pareto smoothed
importance sampling (PSIS), a new procedure for regularizing importance weights.
As a byproduct of our calculations, we also obtain approximate standard errors
for estimated predictive errors and for comparing predictive errors between two
models.

As of version `2.0.0`, the package also provides methods for using stacking and
other model weighting techiques to average Bayesian predictive distributions. 
For details on stacking and model weighting see: 

* Yao, Y., Vehtari, A., Simpson, D., and Gelman, A. (2018). Using
stacking to average Bayesian predictive distributions. In Bayesian
Analysis, doi:10.1214/17-BA1091. 
[Online](https://projecteuclid.org/euclid.ba/1516093227),
[arXiv preprint arXiv:1704.02030](https://arxiv.org/abs/1704.02030).


### Resources

* [mc-stan.org/loo](http://mc-stan.org/loo) (online documentation, vignettes)
* [Ask a question](http://discourse.mc-stan.org) (Stan Forums on Discourse)
* [Open an issue](https://github.com/stan-dev/loo/issues) (GitHub issues for bug reports, feature requests)


### Installation

* Install from CRAN:

```r
install.packages("loo")
```

* Install from GitHub (requires __devtools__ package):

```r
if (!require(devtools)) install.packages("devtools")
devtools::install_github("stan-dev/loo", build_vignettes = TRUE)
```

### Python and Matlab/Octave Code
Corresponding Python and Matlab/Octave code can be found at the
[avehtari/PSIS](https://github.com/avehtari/PSIS) repository.

