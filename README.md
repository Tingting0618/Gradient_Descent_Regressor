# Gradient Descent Regressor

### Main Concept of GD: 

- Gradient Descent is a generic optimization algorithm capable of finding optimal solutions to a wide range of problems. The general idea of Gradient Descent is to **tweak parameters iteratively** in order to minimize a cost function.

- An important parameter in Gradient Descent is the size of the steps, determined by the **learning rate** hyperparameter. If the learning rate is too small, then the algorithm will have to go through many iterations to converge, which will take a long time. If the learning rate is too high, it might jump across and might make the algorithm diverge.

- When using Gradient Descent, you should ensure that all features have a **similar scale** (e.g., using Scikit-Learn’s StandardScaler class), or else it will take much longer to converge.

- SGDRegressor class defaults to optimizing the squared error cost function.

### Types of GD: 
- Batch GD: Computing the gradients based on the full training set
- Stochastic GD: Computing the gradients based on just one instance
- Mini-batch GD: Computing the gradients on small random sets of instances called mini-batches.

### Procedures:

#### 1. Simulate some random data

```Python
import numpy as np
X = 2 * np.random.rand(100, 1)
y = 4 + 3 * X + np.random.randn(100, 1)
```

![download (1)](https://user-images.githubusercontent.com/44503223/127771210-ee8c87ad-934e-48c4-b333-b293879dd9fd.png)


#### 2. Perform Linear Regression using Scikit-Learn

The following code runs for maximum 1,000 epochs or until the loss drops by less than 0.001 during one epoch (max_iter=1000, tol=1e-3). It starts with a learning rate of 0.1 (eta0=0.1), using the default learning schedule (different from the preceding one). Lastly, it does not use any regularization (penalty=None; more details on this shortly):

```Python
sgd_reg = SGDRegressor(max_iter=1000, tol=1e-3, penalty=None, eta0=0.1)
sgd_reg.fit(X, y.ravel())
sgd_reg.intercept_, sgd_reg.coef_
y_predict = sgd_reg.predict(X)
```

#### 3. Visualize the results

![download](https://user-images.githubusercontent.com/44503223/127772672-9a827d38-ea9a-454a-9e7a-7074e49f87d9.png)


## Learn More

For more information, please check out the [Project Portfolio](https://tingting0618.github.io).

## Reference

This repo is my learning journal following:
- Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd Edition, by Aurélien Géron (O’Reilly). Copyright 2019 Kiwisoft S.A.S., 978-1-492-03264-9.
