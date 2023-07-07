# Machine_Learning_task_1 : Linear_Regression

Contains the code for Linear Regression required for the task of Machine Learning

A class for Linear Regression has been created, named Linear_Regression(), with 2 methods: .train(...) and .predict(...)
Parameters for .train(...): 
                            X_train -> Training features of shape (N, D), where N is the number of training examples
                            y_train -> Training labels of shape (N,)
                            learning_rate -> Learning rate for gradient descent, type : float
                            num_iters -> Number of iterations of batch gradient descent, type : integer
                            verbose -> bool type variable for showing loss, along with a graph, at set intervals of number of iterations, type : bool
                            show_at -> iterations after which loss and graph is to be shown, applicable only if verbose = True, type : integer

.train(...) standardizes training features and runs batch gradient descent. Cost function used is Mean Squared Error : 1/N * Summation( (y - y_train) ^ 2), where y is the predicted training label and y_train is the training label. 

Parameters for .predict(...): 
                            X_test -> Features for Test set of shape (N, D), where N is the number of testing examples
                    returns y_pred -> Predicted labels of Test set of shape (N,)

.predict(...) standardizes testing features w.r.t mean and standard deviation of training features.

Metric used for calculating accuracy is Root Mean Squared Error (RMSE) calculated as : ( 1/N * Summation( (y_pred - y_test) ^ 2)) ^ (0.5) , where y_pred is the predicted test label and y_test is the test label. 

RMSE for test data = 3.07130626802989
