# Multiple-Linear-Regression
The ML algorithm allows to predict petrol consumption based on multiple features.

Similar to simple linear regression, here also we are predicting the target variable but it has more than one feature unlike simple linear regression. The features in this model are Petrol_tax, Average_income, Paved_Highways and Population_Driver_licence(%). This model also covers all 6 jars of ML algorithm.

- 1st JAR: Data - 
  - Data Cleaning:
    - Import Data
    - Check for any outliers (iqr method) in each feature and perform clipping the feature between upper and lower threshold in case of outliers
    - Check for missing value, check for data type of each column of dataframe
    - Check for Linear Relationship between each Feature and Target. In case there is not a linear relationship between any feature and target, we try all transformation to achieve linear relationship. The transformation performed are x^2, x^3, x^0.5, e^x and log(x). Still unable to get a linear relation, we delete the feature from the dataset.
    - Checking for duplicates in the Dataset
  - Splitting:
    Split all the features and target dataset into two: Train Data & Test Data
    we would get 4 subsets:
      - Features - Training Dataset
      - Features - Testing Dataset
      - Target - Training Dataset 
      - Target - Testing Dataset
    Here, we have allocated 80% of data for Training and 20% of data for Testing
  - Scaling: 
    We scale the both the features in training and test dataset, need not scale the target dataset.
   
- 2nd JAR: Task - 
  Linear Regression comes under Supervised learning since we are predicting a target.
  From sklearn library, under linear_model module, we are importing LinearRegression
  Then we are assigning an object to LinearRegression
  Later, we fit the object on the scaled feature training dataset and target training dataset
- 3rd JAR: Model -
  We arrive at a mathematical formula containing features and target from the calculated parameters 
- 4th JAR: Loss - 
  We are calculating Mean Squared Error on test data to numerically understand how well the model works.
- 5th JAR: Learning -
  Generally, to find the best parameters which could fit the model, ML algorithm performs a method called gradient descend.
  This Jar has been performed in the 3rd Jar itself. So, there is no specific code to perform gradient descent.
- 6th JAR: Evaluation Metric -
   We are calculating an evaluation metric called r-squared which shows how well the data fit the regression model (the goodness of fit).

Note: We can perform feature selection to eliminate features if there are very high number of features. It works in such a way that it eliminates features that has very less impact on the target variable.

  
