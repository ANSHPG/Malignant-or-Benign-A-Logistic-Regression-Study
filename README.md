# Malignant-or-Benign-A-Logistic-Regression-Study

![LR_train](https://github.com/ANSHPG/Malignant-or-Benign-A-Logistic-Regression-Study/assets/132222062/fb22b375-fd88-4ed1-932f-519dfa9b09eb)



I have been working on a logistic regression project from scratch, without relying on external libraries like scikit-learn, to predict whether a patient has breast cancer or not. Typically, breast cancer is classified into two categories: malignant (positive) and benign (negative).

### Project Overview

#### Data Acquisition
I obtained the data from Kaggle's Breast Cancer Wisconsin (Diagnostic) Data Set.

#### Project Phases
The project is divided into two parts:
1. **Algorithm Development**: Creating the logistic regression algorithm from scratch to derive the equation by finding parameters for each feature.
2. **Decision Boundary Plotting**: Visualizing the decision boundary on a scatter plot to help validate the direction and performance of the algorithm.

### Feature Selection
To simplify the decision boundary plotting, I selected two features: 'radius' and 'smoothness'. This choice allows us to plot a 2D decision boundary. However, the algorithm is designed to handle any number of features for improved results. The features are also expanded into different polynomial degrees to enhance the model's performance.

![LR_test](https://github.com/ANSHPG/Malignant-or-Benign-A-Logistic-Regression-Study/assets/132222062/77cbffaa-24b8-4ee7-8858-0da3e28de15e)

### Key Processes

1. **Sigmoid Function**: 1/(1+e^-z)
    The sigmoid function returns a value between 0 and 1. The greater the value of \(z\), the closer the output will be to 1, where z = wx + b (with w  and  x as vectors, and x representing the features).

2. **Loss Function**: loss = -y(i).log(f(z)) - (1 - y(i)) .log(1 - f(z))
    This loss function is used to compute the cost function.

### Observations

- **Degree**: Using a polynomial degree of 5 for the two features results in a total of 10 features. Higher degrees led to overfitting.
- **Iterations**: More than 1000 iterations are unnecessary as the cost reduction becomes minimal beyond this point.
- **Learning Rate (\(\alpha\))**: Set to 0.01. Be cautious with higher values as it may lead to overshooting.
  
![COST_VS_ITERATION_100K](https://github.com/ANSHPG/Malignant-or-Benign-A-Logistic-Regression-Study/assets/132222062/9369ee25-2a12-488c-8771-19f3ec693c31) ![overshooting_alpha](https://github.com/ANSHPG/Malignant-or-Benign-A-Logistic-Regression-Study/assets/132222062/d9eb8ca3-0342-4f97-9873-364d2d4daecf)


### Implementation
I have structured the algorithm like a package. You only need to specify the features you want to use, the polynomial degree, and the number of iterations. The algorithm will handle everything else, including generating the appropriate parameter values and plotting the decision boundary.

### Minimal Use of External Libraries
To ensure a better understanding, I have kept the use of external libraries to a minimum, primarily utilizing NumPy.

### Repository
The repository, maintained by Anshuman Pattnaik, is publicly available for use. 

Happy coding!
