
# Tanzania Water Pump Prediction

### Introduction
Conducted by Brayton Hall.

- [Data](#data)
- [EDA](#eda)
- [Model](#model)
- [Conclusions](#concl)

## Project Goals
My aim was to predict the functionality of water pumps throughout villages in Tanzania, and perhaps formulate some actionable response from the most important features. 

## Data Collection <a name='data'></a>
The data was obtained from Taarifa (Rwandan News) and the Tanzanian Ministry of Water via the open prediction competition on [drivendata.org](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/). Important features among 40 initial independent variables include:
- pump type
- water quality
- elevation
- region

## EDA <a name='eda'></a>


### Data Cleaning
Many columns were dropped if they had a somewhat duplicate column on which they merely grouped information into broader classes, as well as columns missing many values, resulting in a total of 21 features and 59,400 samples.

### Data Exploration
Medium initial correlations were found between the following features and target variable (status_group): 
Pump type: 0.22
Quality: .16
Elevation: -.11
Region: .11

## Model & Results <a name='model'></a>
used recursive feature engineering with cross validation, linear regression, Lasso L1, Ridge L2, and GridSearchCV to produce our best model : Ridge L2 (alpha: .01) with a root mean squared error of 3.69, meaning it is, on average, 3.69 days off when predicting the true values. 

## Regression Analysis
Recursive feature elimination revealed the most important features in our model, with Income (Composition of Resources) as the main driving factor for life expectancy, followed by Schooling and HIV/AIDS. Our residuals from the model are normally distributed and symmetric, indicating that the assumptions of linearity and homoscedasticity are met. 
### ![residscatter](residualscatter.png)
### ![residdist](residualdist.png)
### ![qqplot](residqq.png)

## Conclusions <a name='concl'></a>
Elevation, Population, Construction year, and Region were the most important features for prediction pump functionality.  


