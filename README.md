Hot Jupiters internal luminosity population inference
========================================

Hot Jupiters population inference based on coupling the observed properties of hot Jupiters to theoretical interior structure models.

This framework was developed and implemented for the paper
`Evidence of Three Mechanisms Explaining the Radius Anomaly of Hot Jupiters`
by Paula Sarkis et al. and submitted to A&A. 
The paper is being reviewed and available upon request.

About the code
--------------

The main goal of this code is to infer the internal luminosity of hot Jupiters 
based on coupling observations to theoretical models. We developed a hierarchical Bayesian model that allows us to make inferences on the population of hot Jupiters within a probabilistic framework.
This framework also allows us to account for the uncertainties on the observed parameters.

The framework is divided into two parts:

1- **Lower Level of the hierarchical model**: Infers the internal luminosity of a single planet.

2- **Upper Level of the hierarchical model**: Inference at the population level



Repo Content
------------

**Code**

The _lower level_  of the probabilistic model is implemented in `single.py` and the _upper level_ in `population.py`.


**Data**

`data` contains all the required data sets to run the code. 

- `interpFn_*`: previously interpolated functions of the theoretical models
- `all_planets-ascii.txt`: the database used in our study 
- `sys_HD_209458`: an example of a dataset in order to run the `SinglePlanetModel`
- `*_chains.csv`: population posterior samples for the different relations `MLR`, `HEET`, `Tint-Teq`, and `Prcb-Teq` using both priors.


**Examples**

All examples are applied to `HD_209458`.

`single_planet_demo.ipynb`: demonstrates how to use the code to infer the internal luminosity distribution of `HD_209458`.

`single_planet_choice_of_prior.ipynb`: shows how to use different priors for the internal luminosity at the _lower level_ and its effect on the inference.

`population_posterior_plots.ipynb`: example code to reproduce some of the figures from the paper.


Dependencies
-------------

- [NumPy](http://www.numpy.org)
- [SciPy](http://www.scipy.org)
- [pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org)
- [scikit-learn](http://scikit-learn.org/stable/)
- [pickle](https://docs.python.org/3.8/library/pickle.html)
- [emcee](https://emcee.readthedocs.io/en/stable/)
- [corner](https://corner.readthedocs.io/en/latest/)
- [Jupyter Notebook](http://jupyter.org)

