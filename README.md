# Lab-2
Install the following python packages needed for this Lab. I would advice that as practice for industry, you install these packages in a virtual environment.

pip install -U scikit-learn pip install pandas pip install numpy pip install jupyterlab pip install matplotlib

This is the second Lab for the class Introduction to Machine Learning DIT 45100 AIW01

You will be provided with some sample code in sample_code.ipynb that should be enough for you to complete the labs. The following tasks below are our objectives for the lab.

You will be implementing the following algorithms we discussed in class:

- Multivariate Linear Regression
  - Implement algorithm i.e: Using python libraries.
  
  - Use LinearRegression class from sklearn
  - ***Feature selection***
       - pearsons correlation 
         - plot correlation matrix
         - Use pearsons correlation to get the best 5 features from our dataset
         - Use LinearRegression to train on the training set and get mse and rsquared on the testing set
       - Use forward feature selection to get the best features with a tol of 0.01
         - Use LinearRegression to to train on the training set and get mse and rsquared on the testing set
       - Use backward elimination to get the best features with a tol of 0.01
         - Use RidgeCV to to train on the training set and get mse and rsquared on the testing set

- Regularized Linear Regression
  - Implement algorithm i.e: Using python libraries.
  
  - Use the Ridge linear model from sklearn
   
   - ***Choose alpha(Regularization parameter)***
     - Split your dataset into a training and testing set
       - Choose the best alpha value for ridge regression using the training set. Use RidgeCV class for this.
       - Use the best model you have with its alpha and get the mse and rsquared on the testing set
       - Plot the loss of the training set and testing set as alpha increases
       
   
       
     
   - ***Learning Curves***
     - Plot a learning curve with increasing training examples by 5.
       - Use RidgeCV to plot the training mse and testing mse as examples increase
   
   - ***Cross Validation***
     - Use k-fold cross validation
       - Use RidgeCV for this.
       - Use k=4
       - calculate the mse and rsquared on the testing sets
       
     - Use ShuffleSplit cross validation
       - Use RidgeCV for this.
       - Use k=4
       - calculate the mse and rsquared on testing sets
       
   - 
