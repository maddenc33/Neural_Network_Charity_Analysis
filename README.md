# Neural_Network_Charity_Analysis

## Module 19 Challenge

#### by Christopher Madden

## Overview

In this module, we'll explore and implement neural networks using the TensorFlow platform in Python. We'll discuss the background and history of computational neurons as well as current implementations of neural networks as they apply to deep learning. We'll discuss the major costs and benefits of different neural networks and compare these costs to traditional machine learning classification and regression models. Additionally, we'll practice implementing neural networks and deep neural networks across a number of different datasets, including image, natural language, and numerical datasets. Finally, we'll learn how to store and retrieve trained models for more robust uses.

To complete the challenge, one must be able to:
- Compare the differences between the traditional machine learning classification and regression models and the neural network models.
- Describe the perceptron model and its components.
- Implement neural network models using TensorFlow.
- Explain how different neural network structures change algorithm performance.
- Preprocess and construct datasets for neural network models.
- Compare the differences between neural network models and deep neural networks.
- Implement deep neural network models using TensorFlow.
- Save trained TensorFlow models for later use.

A foundation, Alphabet Soup, wants to predict where to make investments.  The goal is to use machine learning and neural networks to apply features on a provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  The initial file has 34,000 organizations and a number of columns that capture metadata about each organization from past successful fundings.

## Results

![Img1](https://github.com/maddenc33/Neural_Network_Charity_Analysis/blob/main/Images/Img1.png?raw=true)

**Data Preprocessing**

- What variable(s) are considered the target(s) for your model?
  - The binary variable 'IS_SUCCESSFUL' is the target for the model.
- What variable(s) are considered to be the features for your model?
  - The feature variables are 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS' and 'ASK_AMT'.
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - 'EIN' and 'NAME' are neither targets nor features and could be removed from the input data.

**Compiling, Training, and Evaluating the Model**

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - Layer 1: 120 neurons, relu activation
  - Layer 2: 80 neurons, relu activation
  - Layer 3: 40 neurons, sigmoid activation
  - Layer 4: 20 neurons, sigmoid activation
  - This seemed like a nice mix that I felt might yield positive results.

- Were you able to achieve the target model performance?
  - Target performance of 75.00% was not achieved.  The best performance achieved is 72.41%

![Img2](https://github.com/maddenc33/Neural_Network_Charity_Analysis/blob/main/Images/Img2.png?raw=true)

- What steps did you take to try and increase model performance?
  - I tried increasing the number of layers as well as trying other methods such as tanh activation.  Also, different combinations of activations in different orders with varying numbers of layers.

---

## Summary

The best method I was able to find was to remove the following columns: EIN, STATUS, CLASSIFICATION, and APPLICATION_TYPE.
The next step is to compile, train and evaluate the model as shown below:

![Img3](https://github.com/maddenc33/Neural_Network_Charity_Analysis/blob/main/Images/Img3.png?raw=true)

This increased our accuracy to an acceptable 75.40%

![Img4](https://github.com/maddenc33/Neural_Network_Charity_Analysis/blob/main/Images/Img4.png?raw=true)
