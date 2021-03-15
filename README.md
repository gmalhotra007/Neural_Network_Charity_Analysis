# Neural Network Charity Analysis

## Overview:
---
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
- preprocessing data for a Neural Network Model
- compile, train and evaluate the model
- optimize the model

## Results:
---
#### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
    - Column `IS_SUCCESSFUL` contained binary data referring to whether or not charity donation was used effectively. The variable is considered as the target for our deep learning neural network
    
- What variable(s) are considered to be the features for your model?
    - Columns `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`,`ASK_AMT` were the features 
- What variable(s) are neither targets nor features, and should be removed from the input data?
    - Columns `EIN` and `NAME` were identification information and were dropped from the input data

#### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively
    - The output layer is made of a unique neuron as it is a binary classification.
    - To speed up the training process, we are using the activation function `ReLU` for the hidden layers. As our output is a binary classification, `Sigmoid` is used on the output layer
    - For the compilation, the optimizer is `adam` and the loss function is `binary_crossentropy`

- Were you able to achieve the target model performance?
    - The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations

- What steps did you take to try and increase model performance?
    - To increase the performance of the model, we applied bucketing to the feature `ASK_AMT` and organized the different values by intervals
    - Also, increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers

## Summary:
---
- The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming
- Since we are in a binary classification situation, we could use a supervised machine learning model such as the `Random Forest Classifier` to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model