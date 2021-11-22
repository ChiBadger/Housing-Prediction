# Ames, Iowa Housing Price Prediction Project

### Introduction

The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 80 columns of different features relating to houses.

Three Regression Model will be used in this project to predict the housing prices. 
    - Linear Regression Model 
    - Lasso Regression Model 
    - Ridge Regression Model 

Secondly, The following question will be answered after our model selection. 
    - What feature is the most important feature for house buyers to consider? 
    - what feature add the most value to a home? 
    - what can home seller do to a home to improve the house market price?

### Executive Summary

Datasets were cleaned side by side for training and testing data. There are many columns combined as one feature during our feature engineering processes. Additionally, the cleaning process also include remove NAs and outliers which would impact our model performances. Also, ordinal columns are transferred to numerical based on a scale that indicates the quality of different perspective of the house. Also, all categorical columns were converted to numerical by using Pandas `get_dummies` functions. 

After clearning the data, `train_test_split` has been implemented prior to the modeling processes. After that, All features are being used to all 3 models. By compare the MSE, Lasso has the most accurate result. Now, the feature utilizing process started based upon the `lasso.coef_` calculated in the first round. Feature with low coefficient has been filter out. After a few tests on the filter. We receive the best result on our models. and Lasso perform the best result among other 2 models.

### Findings/Conclusions
Based on the Lasso Cofficient, we can conclude, that `Gr Liv Area` has the largest positivly impact the housing price. And `Exterior 1st_AsbShng` which is Asbestos Shingles largest negatively impact the housing prices.

In addition, `remod age` also negatively impact the housing price. Therefore, a advice can be conclude to house sellers that remodel the house can increase the house price. `Exterior 1st_AsbShng` represent a roofing material called 'Asbestos Shingles' which is a very popular meterical in 1990s. This is also a indication the house may be old.

House Buyer tend to buy a newer house which also indicated on other features represents house qualities. In another word, newer house tend to have a better condition. 


### Data Dictionary
A full description of the data used can be found here: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt