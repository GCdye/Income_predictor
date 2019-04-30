# Income_predictor
A machine learning experiment for predicting incomes
## Problem statement
Build a model to predict if someone will make greater than or less than $50,000 given their:
Age
Education level
Occupation, working class, hours per week
Marital status, race, sex

### Part - 1: Manipulating data
* Added column headers to the data set based on what is described in adult_attributes.txt.
* There are null values.4262 missing data is represented with " ?".
* Removed dashes in the native country names and replace with spaces.
* 14 percent of adults (age 18+) who at most have a High School degree.

### Part - 2: Data Visualization
* Education, age, hours worked, and capital gain have the highest correlation with Income.
* capital_gain’ and ‘fnlwgt’ were highly correlated so we decided to use only one of those variables in the model.


### Part - 3: Building a Model
For this project we tried three models with pretty similar scores. To get a baseline performance We started with logistic regression. Followed by a random decision foreest and ultimately and ADABoost model to give us a final accuracy score of 86%. This was over ten percent increase on the baseline accuracy of 75%. To prep our data for the model we scaled using standard scaler from sklearn, and to boost our performance we added polynomial features. All steps contributed to a better model.

### Part - 4: Excutive Summary
We built a model to predict if someone will make greater than or less than $50,000 given their age, education level, occupation, working class, hours per week, marital status, race and sex. The dataframe we recieved had no columns so when assigning the  we cleaned the data by removing the "?" which we turned into null values. We plotted our data. We tried 3 models: Random Forest, Logisitic Regression and ADAboost with a Decision Tree Classifier. The best score came from random forest classifier model.
