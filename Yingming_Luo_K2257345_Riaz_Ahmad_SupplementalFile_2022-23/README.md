# General note:
All of the source code required for this project is included within the **numerical_methods_comparison.ipynb** Jupyter notebook.

Apart from the widely used open source packages such as Numpy, Matplotlib, Pandas and Scipy, this project makes use of no other external frameworks.

Methods of simulations have been written in OOP style to ensure extendability for further testing and modifications.

# Function classes:
## BaseSimulator
This is the base class for defining random walk models. Consisting of methods for calculating vanilla European option price based on Monte Carlo simulation and function to plot the realisations. However, all child classes must defined the relevant procedure for generating sample paths.

## Euler_discretisation_fast_simulator
This is a class for implementing Euler Scheme random walk model, which inherits the BaseSimulator class.

## Euler_Maruyama_fast_simulator
Class for implementing Euler-Maruyama random walk model, which inherits the BaseSimulator class.

## Milstein_fast_simulator
Class for implementing Milstein's method random walk model, which inherits the BaseSimulator class.

## MC_simulator_optimised
This is the base class for implementing Monte Carlo simulations.

## BarrierOption
Class for implementing Barrier option, inherits the MC_simulator_optimised class. Consist of functions for estimating all 8 types of Barrier Options.

## AsianOption
Class for implementing Asiann option, inherits the MC_simulator_optimised class. Consist of functions for estimating all 4 types of Asian options.

