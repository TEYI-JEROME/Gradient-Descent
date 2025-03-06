# Gradient-Descent

# Gradient Descent for Linear Regression  

This document explains the process of implementing gradient descent for optimizing a linear regression model using the `gradient_descent_reg` class. The class provides a structured approach to training the model, updating weights, and assessing performance through metrics like the Mean Squared Error (MSE).  

## Overview  

Gradient descent is an iterative optimization algorithm used to minimize a function by adjusting the parameters (weights) of the model to reduce the difference between predicted and actual outputs. In the context of linear regression, this involves finding the best-fitting line that minimizes the error between predicted values and actual target values.  

## Key Components of the Implementation  

### 1. Class Structure  

The class `gradient_descent_reg` encapsulates all functionality related to gradient descent for linear regression. It is designed with several important methods:  

- **Initialization**: Sets up the model parameters, including input features, target weights, learning rate, and more.  
- **Loss Function**: Computes the MSE, which quantifies the difference between predicted and actual values.  
- **Gradient Calculation**: Derives the slope of the loss function to determine how to adjust the weights.  
- **Weight Update**: Applies the gradient descent update rule to refine the weights iteratively over a specified number of iterations.  
- **Training Method**: Combines the initialization and update processes in the `fit` method.  
- **Visualization**: Plots the loss over iterations to help visualize the convergence process.  

### 2. Initialization  

When creating an instance of the `gradient_descent_reg` class, you provide the necessary parameters, including:  

- **Input features (x)**: The data used to train the model.  
- **Final weights (w_final)**: The desired output values that the model is trying to predict.  
- **Learning rate (alpha)**: A scalar that dictates the step size of updates to the weights during training.  
- **Decay rate**: An optional parameter controlling how the learning rate decreases over time to facilitate convergence.  
- **Number of iterations (n_iters)**: The total number of updates to perform during the training process.  

### 3. Training Process  

The core of the process is in the `fit` method, which performs the following steps:  

1. **Initialization of Theta**: The starting value of the parameter `theta` is either randomly chosen or set to a specified value.  
2. **Iterative Updates**: For a set number of iterations:  
   - **Calculate Loss**: The MSE is computed based on the current value of `theta`.  
   - **Compute Gradient**: The gradient of the loss function is calculated to determine the direction of the weight adjustment.  
   - **Update Weights**: The current value of `theta` is updated by stepping in the direction of the negative gradient, scaled by the learning rate.  
3. **Store Theta Values**: Throughout the iterations, `theta` values are stored to visualize the training process later.  

### 4. Learning Rate Decay  

In the `fit_decay_1` method, the learning rate is updated at each iteration according to a specified decay strategy. This can help the optimization process stabilize and improve convergence as the algorithm progresses.  

### 5. Visualization  

The `plot` method visualizes the progression of the loss function over iterations. By plotting the loss against the number of iterations, you can observe whether the model is converging towards a minimum loss value, indicating successful training.  

## Conclusion  

The `gradient_descent_reg` class provides a structured and flexible approach to implementing gradient descent for linear regression. By encapsulating the process in a class, it becomes easier to manage, modify, and reuse code for various datasets. The choice of learning rate, decay strategies, and the ability to visualize the training process make this implementation useful for understanding the mechanics of gradient descent in practice.  

Feel free to explore different learning rates and provide conclusions about the gradient descent convergence.
