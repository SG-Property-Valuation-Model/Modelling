# Problem Statement
Homeowners who are looking to sell their property in Singapore usually have a perceived valuation price of their property that might not match the actual valuation price. This perceived valuation price is often indicative, i.e. determined through prices of similar properties around the region, or historical prices the property was sold at. The actual valuation price, on the other hand, is determined by more factors, for instance, types of amenities nearby, crime rates, and remaining lease. Without a central data source that provides access to all this information, home sellers often fail to look at the factors holistically before pricing their property, thus failing to yield the expected profit they desire. Additionally, tools to get an accurate estimate of price are hard to come by, and home sellers often have to engage property agents who typically charge 2% of the property price to help them in this aspect, incurring greater costs. 

Thus, to assist home sellers in making a more informed decision before pricing their property, our project utilises Machine Learning techniques to produce a predictive system that can determine the best possible valuation price. Additionally, we hope to address the information gap more holistically, as we evaluate property prices by looking beyond transactional data sources and considering other factors like safety and convenience. 

Hence, in this repository, we will aim to predict the `Unit Price ($ PSM)` of properties as the target variable of our modelling. For the scope of this project, we will only be working with resale Apartments, Condominiums and Executive Condominiums with a leasehold tenure within Singapore. 


# Description
This repository contains project codes used in the data analysis and model experimentation portion of our project. 


# Data Sources
- Dataset of resale transactions and property price index (PPI) from Real Estate Information System (REALIS) provided by the Urban Redevelopment Authority of Singapore (URA)
- Geographic information from OneMap API developed by the Singapore Land Authority (SLA)
- All other information are from Data.gov.sg
For more detailed information regarding our datafiles, please refer to [this](https://github.com/SG-Property-Valuation-Model/Modelling/blob/main/Overview%20of%20Data%20Files.pdf)

# Models
As  the dependent variable that we're predicting is continuous rather than in nature, we experimented with a variety of regression models. They range from a baseline Linear Regression, which is parsimonious and interpretable, to ones that are more complex such as Ensemble Learning Methods which use several techniques like Bagging, Boosting, and Stacking. We also looked into Neural Networks as they can learn the complex and non-linear patterns in a large dataset. Following are the models we have experimented with:

| Model Type | Model|
| :-------------------------: |---------------|
| Regression | Linear Regression (Baseline), Ridge Regression, Lasso Regression, Elastic Net (Enet) Regression, Support Vector Regression (SVR) |
| Ensemble | Random Forest Regressor (RF), LightGBM Regressor, XGBoost Regressor, Stacking Regressor |
| Neural Network | Feed Forward Neural Network |

# Evaluation Metrics
As our project focuses on predicting the **price of a property per square meter**, the outcome variable is in the form of a continuous value within a given range. Hence, we will be looking into two performance metrics to evaluate our regression model: 
- Root Mean Square Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

| Metric | Objective |
| :----------------------------: |---------------|
| Root Mean Squared Error (RMSE) | RMSE is the most widely used metric for a regression task. It is measured by taking the square root of the averaged squared difference between the predicted output and the actual target value. It is preferred in the case of our project as it not only imposes a larger penalty on errors with a larger magnitude but also allows for easier comparison of errors with the predicted value on the same scale. |
| Mean Absolute Percentage Error (MAPE) | MAPE is expressed as a percentage, which is scale-independent and allows comparison of predicted values on different scales. It offers greater interpretability of error for the sellers as the margin of error is relative to the actual value. |

# Final Model Performance
Out of all the models that we experimented with, XGBoost performed best. Our tuned <b>XGBoost Regressor</b> predicts <b>unit price ($ PSM)</b> with a performance of: 
- Mean Absolute Percentage Error (MAPE) of 4.31%
- Root Mean Square Error (RMSE) of 794.80


# Authors
- Cheryl Yeo Chin Yin - [cherylxyeo1998](https://github.com/cherylxyeo1998)
- Chia Phui Yee Tricia - [triciacpy](https://github.com/triciacpy)
- Ho Mun Yee, Mindy - [myndii](https://github.com/myndii)
- See Hui Yee - [huiyeesee](https://github.com/huiyeesee)
- Zhou Kai Jing - [jayzhoukj](https://github.com/jayzhoukj)


