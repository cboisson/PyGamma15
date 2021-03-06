# Tutorial - Statistics for gamma-ray astronomy

* Presenter: [Michael Schmelling](michael-mpik) and [Christoph Deil](https://github.com/cdeil)
* Duration: 90 min
* Time: Tuesday, 14:00 - 15:30
* Location: Central seminar room

## Abstract

This tutorial will extend the material presented at the [statistics
talk](https://github.com/gammapy/2015-MPIK-Workshop/tree/gh-pages/talks/analysis-stats)
on Monday with a hands-on introduction and exercises.

Participants will be given some example data and implement their own
model and likelihood function as Python functions and perform statistical
analyses using [iminuit](http://iminuit.readthedocs.org/en/latest/).
and [emcee](http://dan.iel.fm/emcee/current/).

An IPython notebook will be used with explanatory text and some code
to get started and participants will implement the analysis.
After the tutorial an IPython notebook with a full solution will be posted
on Github.

Participants get to choose their own adventure:
- Either chi^2 statistic fit of a spectral model (Power-law and cutoff PL) on flux points
- Or Cash statistic fit of a morphology model (Gaussian) on a 2D image

As an optional part we'll have exercises for advanced users to
- implement the same analysis with lower-level tools (optimizer and root-finder only)
  using [scipy.optimize](http://docs.scipy.org/doc/scipy/reference/optimize.html)
- implement the same analysis using [Sherpa](http://cxc.cfa.harvard.edu/contrib/sherpa/)
  (cross-check what iminuit and emcee are doing ...)
- perform an MC simulation and check if the parameter confidence interval coverage is correct
  and if estimators are biased with this example.


## How to prepare

To participate in this tutorial, you have to have a working scientific Python
installation (Python, IPython including notebook, iminuit, emcee and a few other packages).

The full list of packages is given in the [setup-check.ipynb](https://github.com/gammapy/PyGamma15/blob/gh-pages/tutorials/analysis-stats/setup-check.ipynb)
IPython notebook and you can also use that to check that everything is working correctly:

    git clone git@github.com:gammapy/PyGamma15.git
    cd PyGamma15/tutorials/analysis-stats
    ipython notebook setup-check.ipynb

It doesn't matter if you use Python 2 or 3 for this tutorial,
everything will work the same.

## Agenda

- Make sure everyone has the required software working
- Then we'll iterate in these steps: explanation, exercise, present solution
- The steps will probably be:
  - Implement and visualise source model
  - Implement and visualise cost function
  - Estimate parameters with iminuit
  - Estimate parameter errors with iminuit
  - Estimate parameters with emcee
  - Estimate parameter errors with emcee
  - Compare results from iminuit and emcee
- Maybe some optional extra stuff:
  - compute source significance
  - check if parameter estimates are biased and if coverage is correct
- Full solution will be given at the end.

## Going further

If you'd like to learn more, here's some references:

- [References from the stats talk](https://github.com/gammapy/PyGamma15/tree/gh-pages/talks/analysis-stats#references)
