# Lab-2
Install the following python packages needed for this Lab. I would advice that as practice for industry, you install these packages in a virtual environment.

`pip install -U scikit-learn` `pip install pandas` `pip install numpy` `pip install jupyterlab` `pip install matplotlib`, `pip install seaborn`

This is the second Lab for the class Introduction to Machine Learning DIT 45100 AIW01

You will be provided with some sample code in sample_code.ipynb that should be enough for you to complete the labs. The following tasks below are our objectives for the lab.

You will be implementing the following algorithms we discussed in class:

- Multivariate Linear Regression (30 marks)
  - Implement algorithm i.e: Using python libraries.
  
  - Use LinearRegression class from sklearn
  - ***Feature selection:***
       - ***pearsons correlation:*** 
         - plot correlation matrix for all features
         - Use pearsons correlation to get the best 5 features from our dataset
         - Use LinearRegression to train on the training set and get mse and rsquared on the testing set
         - Show which 5 features were selected
       - ***forward selection:*** 
         - Use forward feature selection to get the best features with a tol of 0.01 for mean squared error
         - Use LinearRegression to to train on the training set and get mse and rsquared on the testing set
         - show which features were selected 
       - ***backward elimination:***
         - Use backward elimination to get the best features with a tol of 0.01 for mean squared error
         - Use LinearRegression to to train on the training set and get mse and rsquared on the testing set
         - show which features were selected
       - ***recursive feature elimination:***
         - Use recursive feature elimination to get the best 5 features
         - Use LinearRegression to to train on the training set and get mse and rsquared on the testing set
         - show which features were selected
        
  - ***Cross Validation:***
       - Use ShuffleSplit cross validation
         - Use LinearRegression for this.
         - Use n_splits=4
         - Use 25% of the data for the testing set
         - calculate the mse and rsquared on the testing sets

- Regularized Linear Regression (25 marks)
  - Implement algorithm i.e: Using python libraries.
  
  - Use the Ridge linear model from sklearn
   
   - ***Choosing alpha(Regularization parameter)***
       - Use alpha value of [0.001, 0.01, 0.1, 1] with RidgeCV Regression.
         - Find what it proposed was the best alpha and use that to get the mse and rsquared on the testing set
         - Store and print best alpha found
        
       - ***Cross Validation***
         - Use ShuffleSplit cross validation
         - Use n_splits=4
         - Use 25% of the data for the testing set
         - Use best aplha value you got with normal RidgeRegression. Calculate the mse and rsquared on the testing sets
         - Use alpha value of [0.001, 0.01, 0.1, 1] with RidgeCV Regression. Calculate the mse and rsquared on the testing sets. Print proposed alpha value for each              train and test set
     
   - ***Learning Curves***
     - Plot a learning curve with increasing training examples by 1.
       - Use RidgeRegression with the proposed best alpha to plot the training mse and testing mse as examples increase by 1.
       
- Lasso (10 marks)
  - Implement algorithm i.e: Using python libraries.
  - Use the Lasso linear model from sklearn
   
   - ***Choosing alpha(Regularization parameter)***
       - Use alpha value of [0.001, 0.01, 0.1, 1] with LassoCV Regression.
         - Split your data into a training and test set
         - Find what it proposed was the best alpha and use that to get the mse and rsquared on the testing set
         - Figure out which features were selected
        
       - ***Cross Validation***
         - Use ShuffleSplit cross validation
         - Use n_splits=4
         - Use best aplha value you got with normal LassoRegression. Calculate the mse and rsquared on the testing sets
         - Use alpha value of [0.001, 0.01, 0.1, 1] with LassoCV Regression. Calculate the mse and rsquared on the testing sets. Print proposed alpha value for each              train and test set
         
- Multinomial Logistic Regression (25 marks)
  
  - Implement algorithm i.e: Using python libraries.
  - Use LogisticRegression class 
  - set parameter 'penalty' to 'none'
  - use 'lbfgs' solver
  - Use MinMaxScaler to scale your features
  - ***Feature selection:***       
      - ***chisquare:*** 
        - Use chisquare test to select the best feature(1 feature) to use .
        - Use LogisticRegression to train on the training set and get accuracy and log_loss on the testing set
        - show which features were selected
      - ***forward selection:***
        - Use forward feature selection to get the best features with a tol of 0.01
        - Use LogisticRegression to train on the training set and get accuracy and log_loss on the testing set
        - show which features were selected
      - ***backward selection:***
        - Use backward feature selection to get the best features with a tol of 0.01
        - Use LogisticRegression to train on the training set and get accuracy and log_loss on the testing set
        - show which features were selected
       - ***recursive feature elimination:***
         - Use recursive feature elimination to get the best 5 features
         - Use LogisticRegression to train on the training set and get accuracy and log_loss on the testing set
         - show which features were selected
         
  - ***Cross Validation:***
       - Use StratifiedShuffleSplit cross validation
       - Use LogisticRegression for this.
       - Use n_splits=4
       - Use 25% of the data for the testing set
       - calculate the log loss and accuracy on testing sets

- Regularized Logistic Regression (10 marks)
   - Implement algorithm i.e: Using python libraries.
   - Use the LogisticRegression class from sklearn
   - use 'lbfgs' solver
   - You may now use the 'penalty' parameter and set it to 'l2'
   - Use MinMaxScaler to scale your features
   
   - ***Choosing alpha(Regularization parameter)***
       - Use alpha value of [0.001, 0.01, 0.1, 1] with LogisticRegressionCV.         
         - Find what it proposed was the best alpha per class and use that to get accuracy and log_loss on the testing set
         - Store and print best alpha found per class
         
       - ***Cross Validation***
         - Use StratifiedShuffleSplit cross validation
         - Use n_splits=4
         - Use alpha value of [0.001, 0.01, 0.1, 1] with LogisticRegressionCV. Calculate the  accuracy and log_loss on the testing sets. Print proposed alpha value per class for each train and test set
     

