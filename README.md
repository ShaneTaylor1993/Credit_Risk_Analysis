# Credit_Risk_Analysis

## Purpose
The purpose of this analysis was to apply maching learning techniques to predict credit risk. The goal was to create a more reliable loan experience as well as a more accurate identification of good loan candidates, which would then lead to lower default rates. Using a dataset from LendingClub, we oversampled the data using the RandomOversampler and SMOTE algorithms and undersampled the data using the ClusterCentroids algorithm. We then used a combination of both algortihms using the over-and-under algorithm, SMOTEENN. Next, we compare the two machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. We then evaluate the performance of the models and reccomend which model should be used to predict credit risk.

## Results

### Logisitic Regression with Various Sampling Methods
Due to having imbalanced classes, we used the Balanced Accuracy score to measure the accuracy of our various models of Logisitic Regression.

#### Balanced Accuracy Score
- The Random Oversampling method's Balanced Accuracy had a score of 0.65 which shows that 65% of the time it was accurate in prediciting high and low risk loan.
- The SMOTE Sampling method's Balanced Accuracy score slightly outperformed the Random Oversampling's method with a score of 0.66.
- The Undersampling method was the worst performing method with a Balanced Accuracy score of 0.54.
- The Combination Sampling method outperformed all other method's with a Balanced Accuracy score of 0.67.

#### Precision and Recall
- Precision for all sampling method's did not perform well with them only correctly predicting high_risk loans with 1% certainty. Which shows that there are a large number of false positives.
- Recall scores for the Random Oversampling method were 0.71 and 0.58 for high risk and low risk loans, respectively.
- Recall scores for the SMOTE Sampling method were 0.63 and 0.68 for high risk and low risk loans, respectively.
- Recall scores for the Undersampling method were 0.69 and 0.40 for high risk and low risk loans, respectively.
- Recall scores for the Combination Sampling were 0.73 and 0.60 for high risk and low risk loans, respectively.
    - This was the highest recall score out of all methods.

### Random Forest and Easy Ensemble classifier

#### Balanced Accuracy Score
- The Random Forest model's Balanced Accuracy score was 0.79 which outperformed all of the Logistic Regression methods.
- The Easy Ensemble Classifier's Balanced Accuracy score was 0.93 which outperformed the Random Forest model and all of the Logistic Regression methods.

#### Precision and Recall
- Precision for the Random Forest and the Easy Ensemble classifier were 0.03 and 0.09, respectively.
- Recall scores for the Random Forest model were 0.70 and 0.87 for high risk and low risk loans, respectively.
- Recall scores for the Easy Ensemble Classifier model were 0.92 and 0.94 for high risk and low risk loans, respectively.

## Summary
In summary, it is more important to identify high risk loans than it is to predict potential low risk loans and the Easy Ensemble Classifier is recommended for LendingClub to use due to its high sensitivity for identifying high risk loans. Although the model will have a high number of false positives, it will minimize the amount of flase negatives, which will pose less risk to LendingClub.