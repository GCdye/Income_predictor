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
Logistic Regression: our y ‘income’ is binary.
Random Forest Classifier: because there was a chance of overfitting and it is a more powerful classifier.
AdaBoost with Decision Tree Classifier: we wanted to learn more from our weak features. Most of our features had weak correlation to income so with AdaBoost multiple models are built on top of each other find the best features.

Logistic Regression: Train: 86% and Test: 85% 
Random Forest Classifier: Train: 87% and Test: 86.5%
AdaBoost/ Decision Tree Classifier: Train: 86% and Test: 86%


### Part - 4: Explanation
#### What type of model(s) did you use and why?

Logistic Regression: our y ‘income’ is binary.
Random Forest Classifier: because there was a chance of overfitting and it is a more powerful classifier.
AdaBoost with Decision Tree Classifier: we wanted to learn more from our weak features. Most of our features had weak correlation to income so with AdaBoost multiple models are built on top of each other find the best features.


#### How did you select the variables to be included in the model?

We used all the features except for education-num which was a duplicate column. 

We dummied: 'workclass', 'marital-status', 'occupation', 'relationship', 'race',  'sex', 'income'

We used a mask to seperate US vs the world in terms of income.

#### Did you use any methods for model selection and/or validation? If you are using multiple methods how did you compare the performance of your models?

We ran the models individually and adjusted our parameters to find the best score. We looked at measuring the accuracy for our models against each other. 

#### What is the output of your model and how does it help address the question?
Logistic Regression: Train: 86% and Test: 85% 
Random Forest Classifier: Train: 87% and Test: 86.5%
AdaBoost/ Decision Tree Classifier: Train: 86% and Test: 86%


#### What would you do if you had more time?
PCA, impute the nulls because we did lose 4000 places, create more sub-features of our data.



## Excutive Summary
We built a model to predict if someone will make greater than or less than $50,000 given their age, education level, occupation, working class, hours per week, marital status, race and sex. The dataframe we received had no columns so when reading the dataframe we assigned “No Header” then set the column names from the attached dictionary. We cleaned the data by removing the ‘?’ which we turned into null values. The most difficult decision came from finding what features to keep, dummy and drop. Also there was internal debate about what to do with the the countries of origin, whether to divide by US vs world or divide by continents.  We ran 3 models: Logistic Regression because our y ‘income’ is binary.Random Forest Classifier- because there was a chance of overfitting and it is a more powerful classifier. AdaBoost with Decision Tree Classifier: we wanted to learn more from our weak features. Most of our features had weak correlation to income so with AdaBoost multiple models are built on top of each other find the best features.

Logistic Regression: Train: 86% and Test: 85% 
Random Forest Classifier: Train: 87% and Test: 86.5%
AdaBoost/ Decision Tree Classifier: Train: 86% and Test: 86%

In the end, we found that education and age has the highest correlation to income.