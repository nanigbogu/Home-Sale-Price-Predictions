# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Ames Housing Data and Kaggle Challenge

### Overview

The Ames Housing Dataset contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010. The original data was used for tax assessment purposes but has since been used to predict the sale price of a home. The data has 82 columns which include 23 nominal, 23 ordinal, 14 discrete, 20 continuous variables, 2 observation identifiers, and 2930 observations. 79 of the columns represent home features and each observation represents a sale. ([source](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt))


### Problem Statement

Many homeowners are looking to maximize their value of their home to increase their sale price. Most homeowners only look at what home features can increase the value of their home but neglect to look at what they can do to minimize features that decrease the value of their home. We will explore what home features have an affect on home sale prices.

---

### Datasets

#### Train and Test Datasets

* [`train.csv`](./datasets/train.csv): Train dataset 
* [`test.csv`](./datasets/test.csv): Test dataset

#### Kaggle Submissions

* [`Elastic Net.csv`](./datasets/submissions/EN2.csv)
* [`Lasso.csv`](./datasets/submissions/lasso2.csv)
* [`Ridge.csv`](./datasets/submissions/ridge2.csv)
* [`Lasso Transformed.csv`](./dataset/submissions/lasso_transf.csv)

---

### Data Dictionary

Review the [data descriptions](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

---

## Data Analysis

Dataset was cleaned of outliers, missing values for both categorical and numerical features were filled with the most frequent variable in each column, categorical data was one hot encoded, and everything was scaled to appear more normally distributed.  

The features selected for the models show a strong correlation between 15 numerical features and 12 categorical features. Numerical featuresselected have a correlation of 0.5 or greater with the sale price. Categorial features were evaluated utilizing boxplots and selected based on spread. 

The estimators used to find the best predictor models include linear, lasso, ridge, and elastic net. Each estimator was able to explain at least 89% of the variability in Sale Prices by the features in the model. The best model for this problem utilized Elastic Net because it showed little variance and combined the penalty benefits of both lasso and ridge. It balanced feature elimination and feature coefficient reduction.

---

## Conclusion and Recommendations

Homeowners looking to sell their home should focus on features that will increase the value of their home and combat features that will have a significant decrease in their sale price. The features that have at least a $1,000 impact include increasing home square footage, garage square footage, and/ or masonry veneer square footage; adding baths, porches, a fireplace, and/or central air; updating kitchen, exterior, and/or basement quality. Some of these updates may also improve the overall quality of the home and update add a remodel date that also has a positive impact on the value of a home. Prior to making any of these updates, a homeowner needs to determine the cost to complete some of these updates and what their return on investment would be. Also, they should compare their home to the homes in their neighborhood to get an understanding of sale prices of homes comparable to their own and where they lie in terms of quality of their home.