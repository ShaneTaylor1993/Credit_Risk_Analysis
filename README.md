# Credit_Risk_Analysis

## Purpose
The purpose of this analysis was to apply machine learning techniques to predict credit risk. The goal was to create a more reliable loan experience as well as a more accurate identification of good loan candidates, which would then lead to lower default rates. Using a dataset from LendingClub, we oversampled the data using the RandomOversampler and SMOTE algorithms and undersampled the data using the ClusterCentroids algorithm. We then used a combination of both algorithms using the over-and-under algorithm, SMOTEENN. Next, we compare the two machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. We then evaluate the performance of the models and recommend which model should be used to predict credit risk.

## Results

### Logistic Regression with Various Sampling Methods
Due to having imbalanced classes, we used the Balanced Accuracy score to measure the accuracy of our various models of Logistic Regression.

#### Balanced Accuracy Score
- The Random Oversampling method's Balanced Accuracy had a score of 0.65 which shows that 65% of the time it was accurate in predicting high and low risk loans.
- The SMOTE Sampling method's Balanced Accuracy score slightly outperformed the Random Oversampling's method with a score of 0.66.
- The Undersampling method was the worst performing method with a Balanced Accuracy score of 0.54.
- The Combination Sampling method outperformed all other method's with a Balanced Accuracy score of 0.67.

![BAS](https://user-images.githubusercontent.com/75644168/165717150-199eb640-fd47-4c12-96da-03e5c8f4e1e4.png)


#### Precision and Recall
- Precision for all sampling method's did not perform well with them only correctly predicting high_risk loans with 1% certainty. Which shows that there are many false positives.
- Recall scores for the Random Oversampling method were 0.71 and 0.58 for high risk and low risk loans, respectively.
- Recall scores for the SMOTE Sampling method were 0.63 and 0.68 for high risk and low risk loans, respectively.
- Recall scores for the Undersampling method were 0.69 and 0.40 for high risk and low risk loans, respectively.
- Recall scores for the Combination Sampling were 0.73 and 0.60 for high risk and low risk loans, respectively.
    - This was the highest recall score out of all methods.

![Comparisons](https://user-images.githubusercontent.com/75644168/165717334-1c4ba7ce-e650-4e26-a2a4-9dea88d685d5.png)

### Random Forest and Easy Ensemble classifier

#### Balanced Accuracy Score
- The Random Forest model's Balanced Accuracy score was 0.79 which outperformed all of the Logistic Regression methods.
- The Easy Ensemble Classifier's Balanced Accuracy score was 0.93 which outperformed the Random Forest model and all Logistic Regression methods.

![BRFC_EE_BAS](https://user-images.githubusercontent.com/75644168/165717472-6a2db262-5ed3-4ef2-b32e-250c21d8a302.png)


#### Precision and Recall
- Precision for the Random Forest and the Easy Ensemble classifier were 0.03 and 0.09, respectively.
- Recall scores for the Random Forest model were 0.70 and 0.87 for high risk and low risk loans, respectively.
- Recall scores for the Easy Ensemble Classifier model were 0.92 and 0.94 for high risk and low risk loans, respectively.

![BRFC_EE_Comparison](https://user-images.githubusercontent.com/75644168/165717550-b5341026-1dc5-45d0-b23e-29da762cd2ab.png)


## Summary
In summary, it is more important to identify high risk loans than it is to predict potential low risk loans and the Easy Ensemble Classifier is recommended for LendingClub to use due to its high sensitivity for identifying high risk loans. Although the model will have a high number of false positives, it will minimize the amount of false negatives, which will pose less risk to LendingClub.
