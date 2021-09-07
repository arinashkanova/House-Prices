# Description
This project based on [kagggle competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques).  
This is a perfect competition for data science students who have completed an online course in machine learning and are looking to expand their skill set before trying a featured competition. 

**Practice Skills:**
-  Primary analysis and preprocessing data;
-  Creative feature engineering;
-  Advanced regression techniques like random forest and gradient boosting.

# Goal
It is my job to predict the sales price for each house. For each Id in the test set, you must predict the value of the SalePrice variable.

# Data
All data information in [directory](/data).   
[The Ames Housing dataset](http://jse.amstat.org/v19n3/decock.pdf) was compiled by Dean De Cock for use in data science education.

# Score
Submissions are evaluated on **Root-Mean-Squared-Error (RMSE)** between the logarithm of the predicted value and the logarithm of the observed sales price. (Taking logs means that errors in predicting expensive houses and cheap houses will affect the result equally.)

# Steps:
## [Preprocessing data](/house_prices_preprosesing.ipynb):
-  1. Find errors and correct them;
-  2. Consider numerical features and categorical features;
-  3. Analysis the target;
-  4. Evaluate the influence of features on the target;
-  5. Detection features with NaNs and defining ways to work with them;
-  6. Normalization data using StandardScaler from sklearn;
-  7. Add new features
-  8. One-hot encoding of categorical features;
-  9. Saving cleaned data in CSV for further work.
## [Baseline](/house_prices_preprosesing.ipynb)
As basemodel was using [SGDRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html) (Stochastic Gradient Descent).  
There was no goal to achieve highest score, so model is quite simple and score - 0.15563.
## [Model](/house_price_model.ipynb)
As main model was using [LightGBMRegressor](https://lightgbm.readthedocs.io/en/latest). Than i took feature_importances from learning LightGBM and used this features for learning [CatBoostRegressor](https://catboost.ai/docs/concepts/python-reference_catboostregressor.html).
I used GridSearchCV for selection of parameters.
#My Score
###**Place 661/4730 Score 0.12431 (TOP 14%)**###
