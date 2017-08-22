# Purpose of project
(for detail explanation, please visit my web site www.mlact.com in chinese only)

The purpose of this project is a stepping stone for myself to learn Machine Learning through a real life case.   The reason why choosing Hong Kong horse racing is HKJC maintains high quality of data and transparent to public access.  The project was started with excel VBA and SAS using traditional statistic method and move forward to SQL and R for using Machine Learning methods.
The project here only demonstrated part of my work where:
- Number of feature: reduced from 100+ to less than 10
- Modelling method: Only 4 methods used here while more than 10 tested
- Ensemble method: Xgboost stacking model used

The following is the procedures taken and different approach was used.

# 1. Data Collection
Collect data from HKJC and newspaper web sites, including each race result, horse basic information, trackwork etc, approximately 8,000 races and 100,000 rows data (started with Excel VBA and now using R with web page xpath)

# 2. Data Cleaning
Check whether the data set contains NA / missing / Inf and imputing mean / max / min / 0 or being removed as necessary (Started with Excel and now using R)

# 3. Feature Engineering
Merge data tables and extract addition predictors such as speed rating, last phase speed, horse win percentage etc. (Started with Excel VBA and SAS / SQL and now using R)

# 4. Data Transformation
Normalize or scale the data for standardized unit, extracting predictors for next step

# 5. Data Set Preparation
Stratified sampling the whole data set per race and splitting data into train: 75%, %, test: 25%

# 6. Variable Importance
Using Random Forest to find the importance of variable to response

# 7. Predictive model
a.With two – steps conditional logistic regression, where using fundamental predictors to model the basic strength for each horse, then applying public odds for  to predict the probability of winning for each horse in the same race
b.Adopting other Machine Learning method, such as Random Forest, Support Vector Machine,Xgboost with tuned data

# 8. Comparing Different Models
Comparing confusion matrix from different approaches together with the variable importance and cross validation, picking the best modelling method for analysis.  Fine tuning predictors, learning rate, training / testing data set splitting.

# Result
The fundamental model’s accuracy (without applying odds as factor) for predicting winner is slightly lower than public favorite (around 28% accuracy) but the average odds return is higher than the public’s estimation.  In all, the return turns out with a marginal profit.  There is potential to increase the accuracy by enhancing feature engineering and applying more sophisticated algorithm.  However, as too much noise and mankind uncertainty involved in race, it is expected that the accuracy may be lift up by only a few percent as the existing public estimate is fairly efficient.
