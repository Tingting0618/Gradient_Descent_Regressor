# Gradient_Descent_Regressor

## Gradient Descent

### Main Concept of GD: 

- Gradient Descent is a generic optimization algorithm capable of finding optimal solutions to a wide range of problems. The general idea of Gradient Descent is to **tweak parameters iteratively** in order to minimize a cost function.

- An important parameter in Gradient Descent is the size of the steps, determined by the **learning rate** hyperparameter. If the learning rate is too small, then the algorithm will have to go through many iterations to converge, which will take a long time. If the learning rate is too high, it might jump across and might make the algorithm diverge.

- When using Gradient Descent, you should ensure that all features have a **similar scale** (e.g., using Scikit-Learn’s StandardScaler class), or else it will take much longer to converge.

### Types of GD: 
- Batch GD: Computing the gradients based on the full training set
- Stochastic GD: Computing the gradients based on just one instance
- Mini-batch GD: Computing the gradients on small random sets of instances called mini-batches.

## Learn More

For more information, please check out the [Project Portfolio](https://tingting0618.github.io).

## Reference

This repo is my learning journal following:
- Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd Edition, by Aurélien Géron (O’Reilly). Copyright 2019 Kiwisoft S.A.S., 978-1-492-03264-9.
