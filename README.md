# Credit Risk Analysis
## Overview
The purpose of our project was to utilize various techniques to help determine credit worthiness of loan applicants. This issue is particularly unbalanced as "good" loans vastly outnumber "bad" loans. We will use different supervised machine learning models to help predict credit worthiness. These include:
-Oversampling data using RandomOverSampler and SMOTE algorithms
-Undersampling data using ClusterCentroids algorithm
-Combination approach of both oversampling and undersampling with the SMOTEENN algorithm
-Comapring two models, the BalancedRandomForestClassifier and EasyEnsembleClassifier
## Resources
- Data: LoanStats_2019Q1.csv (provided in the module)
- Tools: Python 3.7.10, scikit-learn, Pandas, Numpy, Juypter Notebook
## Results
### RandomOverSampler
This model provided a balanced accuracy score of 0.64. We can see the high risk precision is 0.01 and the sensitivity is 0.60. This places the F1 score at 0.02. Our low risk category had a precision of 1.0, with a sensitivity of 0.68 and an F1 score of 0.81.
### SMOTE Oversampling
This model provided a balanced accuracy score of 0.64. We can see the high risk precision is 0.01 and the sensitivity is 0.60. This places the F1 score at 0.02. Our low risk category had a precision of 1.0, with a sensitivity of 0.68 and an F1 score of 0.81.
### ClusterCentroins Undersampling
This model provided a balanced accuracy score of 0.53. We can see the high risk precision is 0.01 and the sensitivity is 0.61. This places the F1 score at 0.01. Our low risk category had a precision of 1.00, with a sensitivity of 0.45 and an F1 score of 0.62.
### SMOTEENN Combination Sampling
This model provided a balanced accuracy score of 0.64. We can see the high risk precision is 0.01 and the sensitivity is 0.70. This places the F1 score at 0.02. Our low risk category had a precision of 1.00, with a sensitivity of 0.57 and an F1 score of 0.73.
### BalancedRandomForestClassifier
This model provided a balanced accuracy score of 0.79. We can see the high risk precision is 0.04 and the sensitivity is 0.67. This places the F1 score at 0.07. Our low risk category had a precision of 1.00, with a sensitivity of 0.91 and an F1 score of 0.95.
### EasyEnsembleClassifier
This model provided a balanced accuracy score of 0.53. We can see the high risk precision is 0.07 and the sensitivity is 0.91. This places the F1 score at 0.14. Our low risk category had a precision of 1.00, with a sensitivity of 0.94 and an F1 score of 0.97.
## Summary
Each model used had a low precision score in determing high risk credit. Out of each model, the EasyEnsembleClassifier model showed the best overall classification report, particularly in terms of sensitivity. The high risk sensitivity was .91, meaning only about 9% of high risk applicants would result in a "false positive" approval. However, because the precidion for the high risk group is quite low, 0.07, there's a risk of false negatives in this model. Each model represents the same problem in terms of precision, each of them will predict a large set of false negatives. I would suggest the bank look into other machine learning algorithms to determine credit worthiness.
