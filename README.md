# Banking Crises Analysis
This repository analyzes and predicts the banking crises in African countries

The Notebooks are numerically ordered and go from exploratory data analysis, modelling the features and predicting the Banking Crises for 
the next decade.

## Summary of observations

**1. EDA - Feature correlation**

The countries have unequal number of data for each year. Feature correlations between most of the features isn't high. Hence, all the 
features were used.

**2. Feature Engineering**

Since the data is time-series, an analysis of number of lag features to use for predicting were analyzed using Auto-Odds Ratio Function for
categorical and Auto-Correlation for continuous variables; 3 years of lag data was finalized based on analysis.

**3. Model Selection**

Various classifiers were analyzed and the 4 best classifiers were shortlisted:
- Adaboost tree classifier
- Random forest classifier
- Decision tree classifier
- SVM classifier

A grid search cross-validation was carried out on these classifiers and the best model was saved.

**4. Feature Importance and Interpretation**

The AUC-ROC curve was made for all the models and the models were good having an area of *0.99*.

For the selected models, the feature importance was carried out and it's observed that the most important features are:
- Systemic crisis
- Previous years banking crises
- Inflation
- Exchange rate

**5. Future predictions**

For predicting banking crisis from 2014-2024, the features were forecasted. Since the output labels are imbalanced for final modelling,
based on previous analysis, a new model was trained by oversampling the under-represented class.
This highly improves the accuracy to 100% for the Support Vector Classifier and to 99.78% for the remaining 3 classifiers.

## Future Work

Improvement in features forecasted is required to get better predictions. 

The analyzed models can be used for predicting economic instability and guide investor decisions to invest in these countries.
