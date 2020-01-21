# capstone
This repository contains my Capstone Project 1, which I have completed for SpringBoard: Data Science Career track.

# Project Name: Poverty Level Prediction
Many social programs have a hard time making sure the right people are given enough aid. It’s especially tricky when a program focuses on the poorest segment of the population. The world’s poorest typically can’t provide the necessary income and expense records to prove that they qualify.

In Latin America, one popular method uses an algorithm to verify income qualification. It’s called the Proxy Means Test (or PMT). With PMT, agencies use a model that considers a family’s observable household attributes like the material of their walls and ceiling, or the assets found in the home to classify them and predict their level of need.

While this is an improvement, accuracy remains a problem as the region’s population grows and poverty declines.

Beyond Costa Rica, many countries face this same problem of inaccurately assessing social need

This project is an attempt to classify households according to their poverty level and make a model to make predictions of houselholds
under survey.

# Data
Data for this project is taken from Kaggle competition : [Costan Rican Household Poverty Predictions](https://www.kaggle.com/c/costa-rican-household-poverty-prediction/data)

The data contains train and test data set:
Train dataset has 141 variable and one Target Variable. 
**Target** variable contains 4 categories:
          1 = extreme poverty
          2 = moderate poverty
          3 = vulnerable households
          4 = non vulnerable households
          
We have to decide poverty according to households: variable labeled as **idhogar** and accorded as per poverty staus of head of household **parentsco1**



# Brief description of Project:
### Data Cleaning:
1. 3 variables: **rez_esc**, **v18q1**, **v2a1** has missing values
*rez_esc* : Years behind in School
*v18q1*: Number of tablets in household
*v2a1*: Monthly rent payment

We clean this data by general data cleaning algorithms.

### Data Wrangling: 
1. **dependency** , **edjefe**, **edjefa** columns in dataset has been transformed into numerical datatypes by replacing **"No"**
**"Yes"** with **0** and **1**.
2. Re-configured data labels in Target according to poverty level of head of households than individual poverty. This is done by
equalizing poverty level of each member of household as same as head of household.
3. Assigning head of houselholds where head of household is not provided. This is done by assigning every member of household as 
head of household.

### Feature Engineering

1. Feature Engineering is done to combine highly correlated variables and are similar on having impact on Target outcome
2. After combination of features we have designed features like building components, warning variables
### Exploratory Data Analysis

1. We have explored impact of mean education, age and household conditions on poverty level

### Machine Learning model
We have applied Logistic Regression, RandomForestClassifier and cross validation techniques to design a model.

