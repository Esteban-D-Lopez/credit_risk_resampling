# Module 12 Report Template

## Overview of the Analysis

Nowadays, technology companies have become pioneers in the finance industry by using machine learning models for efficient loan origination and underwriting. By being able to assess credit risk using non-traditional methods, fintech firms and other non-traditional financial institutions have been able to extend credit to consumers, merchants, and businesses who may have otherwise not have been able to have access to these credit opportunities. This analysis shows how machine learning models can be used to use data to accurately assess and predict credit risk, as well as adjusting for possible default scenarios and minimize credit risk.  

Credit risk poses a classification problem that’s inherently imbalanced. This is because in most cases, healthy loans easily outnumber risky loans in a particular pool of loans. This analysis uses various techniques to train and evaluate models with imbalanced classes. By using a dataset of historical lending activity from a peer-to-peer lending services company, this analysis builds a model that can identify the creditworthiness of borrowers.

Specifically, the model uses a logistic regression to predict the outcomes of the pool of loans. This is a type of statistical model used for classification and predictive analytics. Logistic regression estimates the probability of an event occurring, in this case, default on a loan, based on a given dataset of independent variables. Logistic regeression models's variabes are either a 0 or a 1, as the model predicts whether an outcome will happen or not.


## Results


* Machine Learning Model 1:
  * Using SKlearn's logistic regresssion model, the historical data for loans is used to fit the model, and then predict the y values for "loan status" in order to predict whether a loan will default or not.
  * Using the original data, the accuracy score test of the model was 95%.
  * The model accurately predicted 100% of the positive loans, and 85% of the default loans. 
  * By counting the number of default loans in the original set, it is evident that there are far more positive loans (75000) than default loans (2500), which could create an oversampling error in the model. 



* Machine Learning Model 2:
  * In order to account for a possible oversampling issue with the model, the eanalysis uses the RandomOversampler module from the imbalanced-learn library in order to resample the data.
  * After resampling the data, the sample of positive and negative loans is now split 50-50 in the set. 
  * Once again, the resampled data is used to fit the model, and then predict the y values for "loan status" in order to predict whether a loan will default or not.
  * Using the re-sampled  data, the accuracy score test of the model was 99%.
  * The model accurately predicted 100% of the positive loans, and 84% of the default loans. Nevertheless, the recal for the resample data for default loans was 99%, higher than the 91% achieved with the orginal data, showing that the resampled model accurately prediced high-risk loans. 

## Summary

* In summary, the analysis accurately depicts the use of machine learning models applied in credit-risk analysis when looking at underlying data in order to make a loan origination and underwriting decision. In this case, the analysis also depicts how models could run into oversampling errors due to imbalanced data. Nevertheless, the analysis also shows how oversampling can be corrected through the proper use of mitigative statistical tools that can correct for a possible oversampling error. 