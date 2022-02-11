---
title: Supervised Learning Implementation
date: 2022-02-11 10:04:56
tags:
- Machine Learning
category:
- Machine Learning
---
# Automatically Tuning Blackbox Regression Models

## Description
> Write a python function that automatically tunes blackbox regression models. 

## Function interface
```
def tune_blackbox_regression_model(algo, data, regularization_method, M, c, K, criterion):
"""
Automatically tunes blackbox regression models. 

Parameters
----------
algo: A function
    a learning algorithm, i.e. a function that takes as input a matrix X(Rn×p) and a vector of responses 
    Y(Rn) and returns a function that maps inputs to outputs, i.e, maps Rp into R 
data: list
    training data X(Rnxp) Y(Rn)
regularization_method: str
    A regularization method that belongs to the set {'Dropout', 'NoiseAddition', 'Robust'}
M: positive int
    indicating the number of Monte Carlo replicates to be used if the method specified is Dropout or NoiseAddition
c: list
    A vector c of column bounds to be used if the method specified is Robust
K: positive int
    indicating the number of CV-folds to be used to tune the amount of regularization
criterion: str
    A criterion to be used to evaluate the method that belongs to the set {'MSE', 'MAD'}
Returns
-------
predictive_model:
    A predictive model that optimizes the specified criterion using the specified 
    method. I.e., if the function were called with Dropout, M = 100, K = 10 and MSE it would find the amount 
    of dropout (with M = 100 random dropout vectors per observation) that minimizes the ten-fold cross-validated 
    MSE and return the learning algorithm trained with this amount of dropout.
""" 
    return None
```
## Implementation
This function won't build all algorithms from scratch since there are too many available ones good to use. This is more like a collection of them but with some customized features. Generally it could used as a handy tool for myself. Nothing big, but should be easy to use. 

### Regression Algorithms 
> A category of regression models. We can actually get a sophisticated view of this from [scikit-learn.org](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning).  
- Linear Models
- Kernel ridge regression
- Support Vector Machines
- Stochastic gradient descent
- Nearest neighbors
- Gaussian Processes
- Decision Trees
- Neural network models (supervised)

### Data
Data format should be uniform. 

### Regularization Method
> To avoid overfitting by adding extra information to it. 
- Lasso
- Ridge
- Dropout 
- Data Augmentation
- Noise Addition (Gaussian noise to input variables, or to activation, weights, gradients, outputs)
> What's the difference between adding noise to input and data augmentation?
- Robust (??????????????)

### Cross validation
> Necessary

### Criterion to evaluate the model
- MSE (Mean Square Error)
- MAD (Mean Absolute Deviation)

## Development steps
### Criterion 
[ ] MSE<br>
[ ] MAD

### Linear models 
> Use different regularization methods

[ ] Lasso<br>
[ ] Ridge<br>
[ ] Noise Augmentation<br>


### Nonlinear models
[ ] NN<br>
[ ] 
