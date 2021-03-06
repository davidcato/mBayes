# **mBayes**
## Bayesian inference with Wolfram Mathematica

**mBayes** aims at helping researchers to effortlessly carry out Bayesian inference within Wolfram Mathematica. Much of the workflow has been automatized. At the moment, **mBayes** explores the posterior on a grid. This works reasonably well for posteriors up to 4-5 dimensions. If the posterior is close to a multivariate Gaussian distribution, then **mBayes** can save a lot of time by exploring only a suitable ellipsoid obtained via the Fisher matrix.
If dealing with high-dimensional degenerate posteriors please consider tools such as [emcee](https://github.com/dfm/emcee) or [CosmoHammer](https://github.com/cosmo-ethz/CosmoHammer).

Have fun,
[Valerio](http://inspirehep.net/author/profile/V.Marra.1)

### Features

At the moment, the following features are implemented:
* multivariate and flat priors
* variables can be easily fixed without editing the glue code
* Fisher matrix approximation for likelihood and posterior
* Fisher and fast numerical evidence
* grid optimization with Fisher
* optimized parallel computation and exportation 
* automatized exportation of results with consistent labeling 
* confidence levels (actual and gaussian)
* combinations of triangular plots
* an mcmc sampler is not yet implemented; coming...

### Usage

To run the code you should use Mathematica 11; earlier version may show some incompatibilities. Do note move the Mathematica files from the relative folders.

Start by opening the notebook *1-exploration.nb*. There you should customize Section 2 (Glue code) and Section 3 (Parameter space and prior). Please read the comments for help. The result is automatically saved in the folder *results-chi2*.

Once the posterior has been explored, you should open *2-analysis.nb*, rename the relevant variables and run everything. The plots and the other products are automatically saved in the folder *results-analysis*.

*1-exploration.nb* and *2-analysis.nb* are distinct so that you may associate a different kernel to them and, for example, run *2-analysis.nb* while *1-exploration.nb* is busy doing something else.

I will put asap a video for a quick overview of **mBayes**' functionalities and workflow.

### Credits

You can use mBayes, or part of it, freely, provided that in your publications you acknowledge its use and cite the paper Camarena & Marra <https://arxiv.org/abs/1805.xxxxx>.
If using the provided JLA catalog, please cite [Betoule et al 2014](https://arxiv.org/abs/1401.4064).


### Known issues

Mathematica 11.3 is much less forgiving than previous versions. When using Mathematica 11.3 the marginalization routines may give some (inconsequential, most of the times) errors.


### Acknowledgements

Valerio Marra acknowledges contributions from [Tiago Castro](http://inspirehep.net/author/profile/T.Castro.1), [Miguel Quartin](http://inspirehep.net/author/profile/M.Quartin.1) and the awesome community of [mathematica.stackexchange](https://mathematica.stackexchange.com). The use of the color palettes developed by Paul Tol (personal.sron.nl/~pault) and [colorbrewer2](http://colorbrewer2.org) is acknowledged.