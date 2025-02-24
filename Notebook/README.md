# Residential Housing Rental Adds Analysis across Canada

## Objective
The goal is to explore 3 different regression models representing the price of residential housing rental adds with the various rental criteria. A thorough analysis will be performed in order to select one model that predict the rental price most accurately. The most accurate model will tested against completely new independent data from 2025 to evaluate its realtime performance,


### Data source
Here is the data source used for the Residential Housing Rental Adds Analysis across Canada

- [rentfaster.ca](https://www.rentfaster.ca/?utm_source=OOH&utm_medium=sign&utm_campaign=ca)

---
### Step 1: Data Cleaning,

Data cleaning is crucial for data analysis. The cleaned data can be found here [Cleaned Dataset](../Data/canada_rent_clean.csv)

1. From the original dataset, only the residential housing rental adds will be kept for the analysis.
2. Columns with information not needed for the analysis will be discarded
3. Similar terms in a column will be replaced.
4. Unavailable rentals will be removed
5. Missing values will be replaced or discarded.

---
### Step 2 : Data Analysis

Data Analysis is necessary to understand the dataset, the various trends, the distribution and the range of the various information available in the dataset.

The investigation of the price with all the type of data available in the dataset (province, city, # of bedrooms, etc.) will provide us information of the utmost importance about the most suitable predictors in our regression model.


---
### Step 3 : Feature Engeneering

Most regression models can only accept numeric values. Therefore, feature engineered is a crucial step to transform categorical columns into numerical columns.

In addition, this is where we will be finding the best predictors of Price for our regression model. Two methods will be use and compared to find the best predictors:
1. Retaining the highest correlated data in regards of Price
2. Using SelectKBest from the Scikit Learn module to find the best predictors

The best predictors will be used to find the best suitable regression model for the Residential Housing Rental Price accross Canada. 

---
### Step 4 : Testing Regression Models

Three regression models will be compare. Here are the three different tool to build the different model.
1. A Linear Regression model
     - LinearRegression from SciKit Learn module
2. A Polynomial Regression model 
     - PolynomialFeatures from SciKit Learn module
3. An Ordinary Least Sqaure Fit Regression model with various degree polynomial combinaison for specific features
     - statsmodels.api

---
### Step 5 : Validation of the Regression Models
A simple cross-validation technique, "The Train - Test Split", was used to evaluate our models performance.

Each model was train on 80% of the dataset, while it was tested on the remaining 20% of the dataset.

The following performance score were calculated for each models and selected features:

- **Mean Absolute Error (MAE):** 

$$\frac 1n\sum_{i=1}^n|y_i-\hat{y}_i|$$

- **Mean Squared Error (MSE:)** 

$$\frac 1n\sum_{i=1}^n(y_i-\hat{y}_i)^2$$

- **Root Mean Squared Error (RMSE):** 

$$\sqrt{\frac 1n\sum_{i=1}^n(y_i-\hat{y}_i)^2}$$

- **The R-square Score:**

$$
R^2 = 1 - \frac{\text{RS}}{\text{TS}}
$$

where RS is the residual sum of squares, defined as:

$$
\text{RS} = \sum (y_{\text{true}} - y_{\text{pred}})^2
$$

and TS is the total sum of squares, defined as:

$$
\text{TS} = \sum (y_{\text{true}} - \bar{y}_{\text{true}})^2
$$

---
### Step 6 : Real-time Validation of the selected Regression Models

