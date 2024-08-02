# neural-network-challenge-2
Predicting employee turnover

## Overview

This project aims to predict job attrition using a multi-output neural network model. The model simultaneously
predicts both the likelihood of attrition and the department an employee belongs to, based on 14 features from the
dataset.

## Dataset

The dataset contains employee information, including demographics, job-related factors, and work environment
details. While the dataset has limitations, it serves as a starting point for exploring the complex issue of job
attrition.

## Model Approach

### Data Preprocessing

* Loaded the dataset and performed initial exploration to understand available features.
* Separated target variables (Attrition and Department) from feature set.
* Selected 14 relevant features for model input.
* Encoded categorical variables and scaled numerical features.

### Model Architecture

The model uses a multi-output neural network with two shared hidden layers and two separate branches:

* Attrition branch: binary classification with sigmoid activation function
* Department branch: multi-class classification with softmax activation function

Each branch has an additional hidden layer to learn representations specific to each task.

### Model Compilation and Training

* Compiled the model using Adam optimizer.
* Chosen appropriate loss functions for each output (binary cross-entropy for attrition, categorical cross-entropy
for department).
* Trained the model for 100 epochs with a batch size of 32, using validation split for monitoring performance.

## Results and Insights

The trained model achieved an accuracy of approximately:

* 80.7% for attrition prediction
* 64.9% for department prediction on the test set

These results suggest that the model has learned some patterns, but there's significant room for improvement.

## Conclusion

This project serves as an initial exploration into predicting job attrition using machine learning techniques.
While the current model shows promise, there are many avenues for improvement. The insights gained from this model
could potentially help organizations identify factors contributing to attrition and develop strategies to improve
employee retention.
