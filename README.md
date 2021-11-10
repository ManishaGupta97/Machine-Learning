# Machine-Learning
In this problem, given a dataset that records house prices of king county. I used this data to explore the facts on which parameters the price depends and built a model 
which will be able to predict price of the house based on the set of parameters.
My Initial hypothesis was:-
The price of the house is dependent on the area of the house and the year built.
The price of the house also depends on the grade of the house.
The price of the house also depends on the number of bedrooms and bathrooms.

Let us do some EDA by plotting the graphs and understanding the variation the price of with respect to the variables.
EDA:- In this process we will analyze and find out the following :
Missing values.
All numerical variables.
Distribution of numerical variables.
All categorical variables.
Distribution of categorical variables.
Outliers.
Relationship between independent and dependent features(Price).	
Results:- We do not have any missing values in our dataset . Hence we go forward with finding out the numerical and categorical variables.
We see that if the house is recently renovated then the price of the house is high.
We plot histograms to check the skewness for continuous numerical  variables. We observe that features have normal distribution and some of them are skewed. If data is skewed we transform it into log normal distribution.
We plot the bar plots to study the relationship of discrete variables with price. The relationship between grade and price is exponential. We can see that all the features have monotonic relationship with Price. We can also see they have a positive correlation. As sqft_living increases the sales price of the house also increases, and same is for rest of the features.
From the EDA process we infer that the initial hypothesis and assumptions made by us were incorrect and the price of house depends on various other factors other than those taken in consideration during the hypothesis.
FEATURE ENGINEERING AND FEATURE SCALING:- 
We apply the following feature engineering steps to improve the performance of the model.
We transform the variable yr_built to the age of house in years.
We have seen that the numerical variables were skewed. We handle them taking the log transform of these variables.
Note : Here we should only take log transform of non-negative and non-zero columns. If we take log of negative and zero columns we might get NaN values.
3.  Feature Scaling :
In this particular dataset we have many features which have different units. Hence it is necessary we do feature scaling to apply a particular machine learning algorithm.
We use MinMaxScaler which scales all the values between 0 and 1.
Note : We need to perform feature engineering on both the datasets i.e. training data and test data.
LINEAR REGRESSION:
We perform a Linear Regression on the featured data and test the model on the featured test data to get the R squared and RMSE score.
Here we consider all the numerical variables in the dataset after feature engineering as the set of predictors and price as the target.
We drop zip code, id and date from the predictors.
