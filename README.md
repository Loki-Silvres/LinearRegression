# Linear Regression

This document outlines the implementation of a **Linear Regression** model for a Machine Learning task. A custom class, `Linear_Regression`, is developed with methods for training and predicting. Below are the details:

---

## Class: `Linear_Regression`

### Methods:
1. **`train()`**
2. **`predict()`**

---

### Method: `.train(...)`

#### **Parameters:**
- **`X_train`**:  
  Training features of shape \((N, D)\), where \(N\) is the number of training examples, and \(D\) is the number of features.
- **`y_train`**:  
  Training labels of shape \((N,)\).
- **`learning_rate`** *(float)*:  
  Learning rate for gradient descent.
- **`num_iters`** *(int)*:  
  Number of iterations for batch gradient descent.
- **`verbose`** *(bool)*:  
  If `True`, displays loss and plots a graph at intervals of iterations specified by `show_at`.
- **`show_at`** *(int)*:  
  Number of iterations after which to display the loss and graph, applicable only if `verbose=True`.

#### **Functionality:**
- **Standardizes** the training features.
- Performs **Batch Gradient Descent** using the **Mean Squared Error (MSE)** as the cost function:  
  MSE = (1/N) * Σ (y - y<sub>train</sub>)²  
where:  
- y = predicted labels  
- y<sub>train</sub> = actual training labels.

---

### Method: `.predict(...)`

#### **Parameters:**
- **`X_test`**:  
  Testing features of shape \((N, D)\), where \(N\) is the number of testing examples.

#### **Returns:**
- **`y_pred`**:  
  Predicted labels for the test set of shape \((N,)\).

#### **Functionality:**
- Standardizes testing features using the **mean** and **standard deviation** of the training features.

---

## Evaluation Metric

- **Root Mean Squared Error (RMSE):**  
  Used to measure accuracy, defined as:  
  RMSE = sqrt((1/N) * Σ (y_pred - y_test)^2)
  where:
  - `y_pred` = predicted labels for test data  
  - `y_test` = actual test labels.

- **Reported RMSE for Test Data:**  
  \[
  RMSE = 3.0713
  \]

---
