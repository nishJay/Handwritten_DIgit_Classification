# Handwritten_Digit_Classification
Image Processing With Python Project

## Problem definition:


Implement image classification for the MNIST handwritten digit database. Your implementation should recognize the digit written by the evaluator.


## Team:

Skanda S Kumar (1MS20CS117)

Ninaad P S     (1MS20IS078)

R Jayanth Jadhav (1MS20IS091)

## Algorithm we are implementing:

Convolutional neural network (CNN) model 

## Model Evaluation Methodology

The dataset already has a well-defined train and test dataset.

In order to estimate the performance of a model for a given training run, we further split the training set into a train and validation dataset.

Performance on the train and validation dataset over each run is then plotted to provide learning curves and insight into how well the model is learning the problem.

The Keras API supports this by specifying the “validation_data” argument to the model.fit() function when training the model, that will, in turn, return an object that describes model performance for the chosen loss and metrics on each training epoch.

In order to estimate the performance of the model on the problem, we use k-fold cross-validation, i.e. five-fold cross-validation. This gives some account of the model's variance with both respect to differences in the training and test datasets, and in terms of the stochastic nature of the learning algorithm. The performance of a model is taken as the mean performance across k-folds, given the standard deviation, that is used to estimate a confidence interval if desired.

We use the KFold class from the scikit-learn API to implement the k-fold cross-validation evaluation of the neural network model.

