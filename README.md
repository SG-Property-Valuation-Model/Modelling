# Problem Statement
Homeowners who are looking to sell their property in Singapore usually have a perceived valuation price of their property that might not match the actual valuation price. This perceived valuation price is often indicative, i.e. determined through prices of similar properties around the region, or historical prices the property was sold at. The actual valuation price, on the other hand, is determined by more factors, for instance, types of amenities nearby, crime rates, and remaining lease. Without a central data source that provides access to all this information, home sellers often fail to look at the factors holistically before pricing their property, thus failing to yield the expected profit they desire. Additionally, tools to get an accurate estimate of price are hard to come by, and home sellers often have to engage property agents who typically charge 2% of the property price to help them in this aspect, incurring greater costs. 

Thus, to assist home sellers in making a more informed decision before pricing their property, our project utilises Machine Learning techniques to produce a predictive system that can determine the best possible valuation price. Our valuation system prides on addressing the information gap more holistically, as we evaluate property prices by looking beyond transactional data sources and considering other factors like safety and convenience. We also integrated our system into a web interface that we have built to ease the process of getting an accurate property valuation and other information such as amenities nearby and current housing prices. 


# Description
This repository contains project codes used in the data analysis and model experimentation portion of our project. 


# Data Sources
- Dataset of resale transactions and property price index (PPI) from Real Estate Information System (REALIS) provided by the Urban Redevelopment Authority of Singapore (URA)
- Geographic information from OneMap API developed by the Singapore Land Authority (SLA)
- All other information are from Data.gov.sg
For more detailed information regarding our datafiles, please refer to [this]

# Models
After which, we delved into experimenting with a variety of models ranging from a baseline Linear Regression, which is parsimonious and interpretable, to ones that are more complex such as Ensemble Learning Methods which use several techniques like Bagging, Boosting, and Stacking. We also looked into Neural Networks as they can learn the complex and non-linear patterns in a large dataset. Following are the models we have experimented with:

| Model Type | Model|
| :--------------: |---------------|
| Regression | Linear Regression (Baseline), Ridge Regression, Lasso Regression, Elastic Net (Enet) Regression, Support Vector Regression (SVR) |
| Ensemble | Random Forest Regressor (RF), LightGBM Regressor, XGBoost Regressor, Stacking Regressor |
| Neural Network | Feed Forward Neural Network |

