# Multiple-Linear-Regression
The ML algorithm allows the prediction of petrol consumption based on multiple features.

Similar to simple linear regression, here also we are predicting the target variable but it has more than one feature, unlike simple linear regression. The features in this model are Petrol_tax, Average_income, Paved_Highways, and Population_Driver_licence(%). This model also covers all 6 jars of the ML algorithm.

- 1st JAR: **Data** - 
  - Data Cleaning:
    - Import Data
    - Check for any outliers (IQR method) in each feature and perform clipping the feature between the upper and lower threshold in case of outliers
    - Check for missing values, check for the data type of each column of the data frame
    - Check for Linear Relationship between each Feature and Target. If there is no linear relationship between any feature and target, we try all transformations to achieve a linear relationship. The transformation performed are x<sup>2</sup>, x<sup>3</sup>, x<sup>0.5</sup>, e<sup>x</sup> and log(x). Still unable to get a linear relation, we delete the feature from the dataset.
    - Checking for duplicates in the Dataset
  - Splitting:
    Split all the features and target dataset into two: Train Data & Test Data
    we would get 4 subsets:
      - Features - Training Dataset
      - Features - Testing Dataset
      - Target - Training Dataset 
      - Target - Testing Dataset
    Here, we have allocated 80% of the data for Training and 20% of data for Testing
  - Scaling: 
    We scale both the features in the training and test dataset but need not scale the target dataset.
   
- 2nd JAR: **Task** - 
  Linear Regression comes under Supervised learning since we are predicting a target.
  From sklearn library, under linear_model module, we are importing LinearRegression.
  Then we are assigning an object to LinearRegression.
  Later, we fit the object on the scaled feature training dataset and target training dataset.
  
- 3rd JAR: **Model** -
  We derive a mathematical formula containing features and target from the calculated parameters.
  
- 4th JAR: **Loss** - 
  We are calculating Mean Squared Error on test data to understand how well the model works numerically.
  
- 5th JAR: **Learning** -
  Generally, to find the best parameters which could fit the model, the ML algorithm performs a method called gradient descent. This is an optimization algorithm that has been performed in the 3rd Jar itself when we derived the model. So, there is no specific code to perform gradient descent.
  
- 6th JAR: **Evaluation Metric** -
   We are calculating an evaluation metric called r-squared which shows how well the data fit the regression model (the goodness of fit).

Note: We can perform feature selection to eliminate features if there are a very high number of features. It works in such a way that it eliminates features that have very less impact on the target variable.

  
