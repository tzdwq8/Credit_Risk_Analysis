# Credit Risk Analysis

## Overview
For this project we used Python to build and evaluate several machine learning models to predict credit risk.  Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.  Therefore, we employed different techniques to train and evaluate models with unbalanced classes.  Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we performed the following:
- Oversampled the data using the **RandomOverSampler** and **SMOTE** algorithms.
- Undersampled the data using the **ClusterCentroids** algorithm.
- Used a combinatorial approach of over and undersampling using the **SMOTEENN** algorithm.
- Compared two machine learning models that reduce bias, **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**.

## Results
### RandonOverSample Model
![ROS Accuracy](https://user-images.githubusercontent.com/85590155/136723305-a9f8c1db-a2ed-483d-b4d3-c143ceb93eb8.PNG)
- The balanced accuracy score was **66%**.  Meaning this model was not very good at predicting credit risk.

![ROS Classification](https://user-images.githubusercontent.com/85590155/136723317-431ab782-2144-4e15-916c-506fd9bb8337.PNG)
- The precision score for low risk loans was **100%**, but only **1%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **67%** and **66%**.

### SMOTE Model
![SMOTE Accuracy](https://user-images.githubusercontent.com/85590155/136723327-60add63e-e185-446f-9892-c77b56e523dc.PNG)
- The balanced accuracy score was **63%**.  Meaning this model was not very good at predicting credit risk.

![SMOTE Classification](https://user-images.githubusercontent.com/85590155/136723333-cf41e1a3-c94a-4c21-ab50-9a6d4235df57.PNG)
- The precision score for low risk loans was **100%**, but only **1%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **64%** and **62%**.

### ClusterCentroids Model
![Under Accuracy](https://user-images.githubusercontent.com/85590155/136723381-99237c61-e1bb-473e-8756-f8168302e7ff.PNG)
- The balanced accuracy score was **51%**.  Meaning this model was not very good at predicting credit risk.

![Under Classification](https://user-images.githubusercontent.com/85590155/136723389-0b85bc12-f9ec-4db1-8bbc-094001b7159d.PNG)
- The precision score for low risk loans was **100%**, but only **1%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **43%** and **59%**.

### SMOTEENN Model
![Combo Accuracy](https://user-images.githubusercontent.com/85590155/136723431-78896096-8bc2-43c0-958d-4adb5275a0f5.PNG)
- The balanced accuracy score was **62%**.  Meaning this model was not very good at predicting credit risk.

![Combo Classification](https://user-images.githubusercontent.com/85590155/136723437-711c8bae-5bb3-4c8c-9b9d-ebf362b3eb73.PNG)
- The precision score for low risk loans was **100%**, but only **1%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **54%** and **70%**.

### BalancedRandomForestClassifier Model
![Forest Accuracy](https://user-images.githubusercontent.com/85590155/136723462-1e44439a-bc9d-4381-bae9-6f3bfa82eb76.PNG)
- The balanced accuracy score was **79%**.  Meaning this model was fair at predicting credit risk.

![Forest Classification](https://user-images.githubusercontent.com/85590155/136723474-4a6f0a5a-f8e8-4e7a-9bb9-c101447c8c85.PNG)
- The precision score for low risk loans was **100%**, but only **4%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **91%** and **67%**.

### EasyEnsembleClassifier Model
![Easy Accuracy](https://user-images.githubusercontent.com/85590155/136723496-e1b175ca-a085-463c-a78a-50a37be50ab4.PNG)
- The balanced accuracy score was **92%**.  Meaning this model performs well at predicting credit risk.

![Easy Classification](https://user-images.githubusercontent.com/85590155/136723503-ee320ba9-6287-46cf-b70c-6eb487c61dc5.PNG)
- The precision score for low risk loans was **100%**, but only **7%** for high risk loans.
- The recall score for low risk and high risk loans, respectively, were **94%** and **91%**.

## Summary
The best performing model was the **EasyEnsembleClassifier**.  When looking at the scores, all but one was above 90%.  The one below 90% was the precision score for high risks loans which was 7%.  This means only 7% of the predicted high risk loans are actually high risk.  However, credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. The balance of the target variables are low risk at 68,470 and high risk at 347.Therefore, even though 93% of the predicted high risk loans are actually low risk, this model would not significantly impact business.  Therefore the recommendation is to use the **EasyEnsembleClassifier** model.
