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

    As part of Data Cleaning process, first, presence of null values have been identified and variables with very high 
    percentage of nulls are dropped since these variables are going to contribute much towards the analysis for prediction. 
    Now, the skewness for the categorical variables have been checked. The variables for which data is highly skewed are
    identified and dropped. With these two steps of data cleaning, the data looks cleaned and no further cleaning is required.
    
Exploratory Data Analysis:

    EDA is performed by using different Data Visualization techniques. Before moving into Visualization, continuous and 
    categorical variables are identified separately.
    Pairplot from seaborn is used to visualize the continuous variables to identify aany sort of correlation present amongst
    the continuous variables with each other.
    Boxplot is used to find if any outlier is present or not. 
    Also, a displot is used to check the distribution of the target variable.
    The categorical variables are visualized using bosplots and a clear influence on the target variable has been identified.
    
Data Preparation:

    
