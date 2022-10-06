# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to use different techniques in order to train and evaluate models with unbalanced classes so we can determine whether or not they should be used to predict credit risk for LendingClub, a peer-to-peer lending services company.

## Results

![naive_random_oversampling](https://user-images.githubusercontent.com/105808695/194404733-ae7f36b1-9827-4dce-987b-50b8a1bb67d1.png)

#### Naïve Random Oversampling

-	Balanced Accuracy Score: 65%
-	Precision:
    - High Risk: 1%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 63%
    - Low Risk: 66%

![smote_oversampling](https://user-images.githubusercontent.com/105808695/194404786-58e0d31c-4031-4555-8a42-96b811f0ffe9.png)

#### SMOTE Oversampling

-	Balanced Accuracy Score: 62%
-	Precision:
    - High Risk: 1%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 62%
    - Low Risk: 63%

![undersampling](https://user-images.githubusercontent.com/105808695/194404834-c0013c6f-effe-452a-af44-166f28a01144.png)

#### Undersampling

-	Balanced Accuracy Score: 51%
-	Precision:
    - High Risk: 1%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 59%
    - Low Risk: 43%

![smoteenn_combination_sampling](https://user-images.githubusercontent.com/105808695/194404876-53ec8509-11aa-47c5-b65a-709e289f53ed.png)

#### SMOTEENN Combination (Over- & Under-) Sampling

-	Balanced Accuracy Score: 65%
-	Precision:
    - High Risk: 1%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 69%
    - Low Risk: 61%

![balanced_random_forest_classifier](https://user-images.githubusercontent.com/105808695/194404902-3d8ccd83-b36d-4935-80c9-d569304b7881.png)

#### Balanced Random Forest Classifier

-	Balanced Accuracy Score: 79%
-	Precision:
    - High Risk: 4%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 67%
    - Low Risk: 91%

![easy_ensemble_adaboost_classifier](https://user-images.githubusercontent.com/105808695/194404936-6393c5fa-02d0-4bdd-bbf7-69484f90da83.png)

#### Easy Ensemble AdaBoost Classifier

-	Balanced Accuracy Score: 93%
-	Precision:
    - High Risk: 7%
    - Low Risk: 100%
-	Recall: 
    - High Risk: 91%
    - Low Risk: 94%

## Summary

For the six models evaluated, we are focusing on the accuracy score, precision, and recall. To help understand what these numbers mean:

- Balanced Accuracy Score = how often the classifier is correct with the model
- Precision: A low precision is indicative of a large number of false positives
- Recall: A low recall is indicative of a large number of false negatives

All of the models had at over 50% for their accuracy score, but the Easy Ensemble AdaBoost Classifier had the most accurate model with 93%. Additionally, every model had high precision for detecting low-risk, yet low precision for detecting high risk. Again, the Easy Ensemble AdaBoost Classifier had the highest precision number out of all of the models with a 7% chance of lowering the amount of false positives. The Easy Ensemble AdaBoost Classifier also returned the highest recall numbers for both high and low risk, with 91% and 94% respectively, which helps to keep the number of false negatives low.

When evaluating for credit risk, it is important to keep the false negatives low. However, another consideration would be that false positives could be preventing loans from going out to low-credit risk customers who have been falsely identified as high risk. At this point, I would recommend using the Easy Ensemble AdaBoost Classifier model for now, but it could be good to keep searching for something that could increase the precision in detecting true high-risk credit.

