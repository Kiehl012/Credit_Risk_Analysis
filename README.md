# Overview: Credit Risk Analysis
The purpose of this analysis was to create 6 machine learning models using different learning and resampling methods to find out which, (if any) produced an effective model for evaluating credit risk. The data used was an unbalanced data set with 68,470 "low-risk" loans and 347 "high-risk" loans. For each loan in the data set, there are 95 vairables like income, interest rate, and loan amount etc. that each model uses to predict whether a given loan is high-risk or low-risk. Four of the models were logistic regression models, each with a different resampling method to deal with the imblanced data. The sampling methods included, random oversampling, SMOTE oversampling, cluster centroid undersampling, and SMOTEENN sampleing (over and under). The final two models utilized ensemble leanring. Specifically, balanced forest classifier and easy ensemble ADAboost classifier. The results of each model can be found below.

# Results
See the results of each model below. Note that in the imbalanced classification report tables, 0 indicates "low-risk" loans and 1 indicates "high-risk" loans.
### - Random Oversampling
#### Balanced Accuracy Score: 0.6579
![Screen Shot 2022-01-29 at 10 03 20 AM](https://user-images.githubusercontent.com/90878911/151667931-5cabb1b3-52ae-4e0d-a5f5-a245acd50837.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was extremely low (~1%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 60% of low-risk loans were identified correctly and 71% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~66% of the loans in test test group.

### - SMOTE Oversampling
#### Balanced Accuracy Score: 0.6622
![Screen Shot 2022-01-29 at 10 50 14 AM](https://user-images.githubusercontent.com/90878911/151669578-fc95c245-d464-4b36-aba9-2bf602e48b3f.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was extremely low (~1%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 69% of low-risk loans were identified correctly and 63% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~66% of the loans in test test group.

### - Cluster Centroid Undersampling
#### Balanced Accuracy Score: 0.5443
![Screen Shot 2022-01-29 at 10 05 48 AM](https://user-images.githubusercontent.com/90878911/151668032-4a95da1f-83f5-4ad7-ace6-e7f865fdf23b.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was extremely low (~1%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 40% of low-risk loans were identified correctly and 69% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~54% of the loans in test test group.

### - Combination (Over and Under) Sampling with SMOTEENN Algorithm
#### Balanced Accuracy Score: 0.6274
![Screen Shot 2022-01-29 at 10 07 14 AM](https://user-images.githubusercontent.com/90878911/151668085-8f239d44-c495-4b22-adb0-0f3354e7293f.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was extremely low (~1%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 59% of low-risk loans were identified correctly and 66% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~62% of the loans in test test group.
 
## Ensemble Learners

### - Balanced Random Forest Classifier
#### Balanced Accuracy Score: 0.7611
![Screen Shot 2022-01-29 at 10 09 19 AM](https://user-images.githubusercontent.com/90878911/151668230-391345af-eeb9-407d-b6d6-84251532d6ed.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was extremely low (~4%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 91% of low-risk loans were identified correctly and 61% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~76% of the loans in test test group.


### - Easy Ensemble AdaBoost Classifier
#### Balanced Accuracy Score: 0.9281
![Screen Shot 2022-01-29 at 11 07 30 AM](https://user-images.githubusercontent.com/90878911/151670172-5e029233-6211-4ce9-b036-0cdb669e3519.png)</br>

The results of this model show that the precision for detecting low-risk loans was very high (~100%), meaning that almost every loan identified as low-risk, was actually low risk. However, the precision for detecting high-risk loans was low (~7%), meaning most of the loans identified as high-risk were not actually high-risk. The recall scores show that about 93% of low-risk loans were identified correctly and 92% of high-risk loans were identified correctly. Finally, we can see from the balanced accuracy score that this model correctly predicted risk level of ~93% of the loans in test test group.

# Summary
Based on the results above, the ensemble learners did much better than the first 4 logistic regressions. The AdaBoost model was the clear stand out with an accuracy score of 93%. However, like all of the other models, the precision of high-risk loan predictions if quite low. The model only predicts high-risk loans accurately about 7% of the time. For this reason, I would not use any of these models by themselves to decide when and when not to grant loans. That being said, because the Adaboost model accurately predicts low-risk loans with high accuracy and sensitivity, this could be a good tool for auto-approving low-risk loans. Loans classified as high-risk could then be set aside for manual review or further analysis.






