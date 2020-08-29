# House Price Prediction
Prediction of Houses based on different variables to help a US-based housing company named Surprise Housing so that they can start investing in the Australian Market. A machine learning model is required to predict the price of the houses with the available variables. The business can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns.Further, the model will be a good way for management to understand the pricing dynamics of a new market.

Below are the libraries and packages used in this Machine Learning model building:-

    1. NumPy
    2. Pandas
    3. Matplotlib
    4. Seaborn
    5. SKLearn

From SKLearn, below packages have been used:- 

    1. train_test_split
    2. RFE (Recusrsive Feature Elimination)
    3. Ridge
    4. Lasso
    5. GridSearchCV
   
Data Collection:

    A file in CSV format has been provided by the US-based housing company, Surprise Housing.
  
Data Cleaning:

    As part of Data Cleaning process, the skewness for the categorical variables have been checked. The variables for which 
    data is highly skewed are identified and dropped. With these two steps of data cleaning, the data looks cleaned and no 
    further cleaning is required.
    
Exploratory Data Analysis:

    EDA is performed by using different Data Visualization techniques. Before moving into Visualization, continuous and 
    categorical variables are identified separately.
    Pairplot from seaborn is used to visualize the continuous variables to identify aany sort of correlation present amongst
    the continuous variables with each other.
    Boxplot is used to find if any outlier is present or not. 
    Also, a displot is used to check the distribution of the target variable.
    The categorical variables are visualized using bosplots and a clear influence on the target variable has been identified.
    
Data Preparation:

    For continuous variables, the variables with missing values are identified. As the number of missing values are not much, we
    impute these missing values with mean.
    For the categorical variables, we first identify the variables with meaningful missing values and impute them accordingly.
    Some of the categorical variables contain more number of categories. So, we use bucketing to handle this situation.
    Then, we dummify the categorical variables and drop the original categorical variables.
    We derive some age variables from date variables present in the dataset.
    The target variable is transformed using log transformation to a normally distributed variable.
    
Model Building:

    Data is split into X and y variables.
    Data is split into train and test set.
    Continuous variables from X set are standardized.
    RFE is used to select top 50 variables.
    GridSearchCV is used for hyperparameter tuning to find the best set of parameters.
    The model is used to predict on the test set. 
    The R-squared is used to evaluate the model.
    

Since, alpha or lambda is the coefficient of the regularization part of the cost function, and our aim in any model is to reduce the value of the cost function, we always choose the model for which the value of alpha/lambda is less. For a good model, the value of alpha tends to zero. The best model’s cost function is equipped with only the error term because in that case the value of alpha/lambda becomes zero.

Here, in this case, in case of Ridge regression, the optimum value of alpha is 5.0. Whereas the optimum value of alpha for Lasso regression is 0.00005. It is clearly shown that for Lasso, the optimum value of alpha is much lesser than that of Ridge.

Hence, in case of Lasso regression, the value of regularization term in the cost function will be lesser than that of Ridge regression. And so, cost function will be lesser for Lasso regression compared to Ridge regression.

Hence, we choose Lasso regression over Ridge regression.
