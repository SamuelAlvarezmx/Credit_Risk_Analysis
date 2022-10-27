# Credit_Risk_Analysis

## Overview

This project focused on using Machine learning and different techniques to train a data set bases on credit cards history and develop different models to learn which model applies a better solution to a real world problem that is credit. 

The different methods of machine learning were resampling models, SMOTEEN algorithms and Ensemble classifiers

## Results

### Naive Random Over Sampling

<img width="708" alt="Screen Shot 2022-10-26 at 16 27 52" src="https://user-images.githubusercontent.com/104656920/198141826-bff478d7-1c3d-4947-b211-5e79375f0243.png">

* The accuracy level is 0.657 which is not a great accuracy.
* We have here a very low precision for high risk loans however this model has a very good precision for low risk loans
* The recall or sensitivity on high risk is .71 which might not seem that bad, however considering this operations are high risk a sensitivity is not as important as precision.

* After looking to the f1 we can see that this model is not as good predicting high risk because have an f1 of 0.01, we do not have an equilibrium between sensitivity and precision. Whereas in low risk loans we can see that this model seems more capable to predict them because of the f1 of .75

### SMOTE oversampling

<img width="1111" alt="Smote_oversampling" src="https://user-images.githubusercontent.com/104656920/198142060-6d1ba058-947a-4edf-8d17-ea91ac31e365.png">

* The accuracy level is 0.662 which is not a great accuracy but better than the later model. 
* We have also a very low precision for high risk loans even worse than before, but the precision for low risk loans still is great.
* The recall or sensitivity on high risk is .63 which is lower than the last one, however comparing low risk loans it ouperforms the Naive random model

* After looking to the f1 we can see that this model is not as good predicting high risk because have an f1 of 0.02, we do not have an equilibrium between sensitivity and precision. Whereas in low risk loans we can see that this model seems more capable to predict them because of the f1 of .82. Being a better model for low risk loans than the one before.

### Undersampling (Cluster Centroids)


<img width="736" alt="undersampling" src="https://user-images.githubusercontent.com/104656920/198142368-baea5db5-8157-40d5-8d03-7a365fb20a6e.png">

* The accuracy level is 0.544, this means it has a low score of total true predictions low and high risk loans are not very well predicted with this model.  
* Once again the precision gor high risk loans is very low 0.01 and the low risk great with a value of 1.
* The recall or sensitivity on high risk is .69 and the sensitivity for low risk loans is .40. Getting a very poor performance in both of the predictions as we can see on the f1 of each of the loan status, getting an .52 each of the status.

### Combined sampling (Over and under sampling)

<img width="754" alt="Screen Shot 2022-10-26 at 16 32 35" src="https://user-images.githubusercontent.com/104656920/198142531-39745e47-68f2-424d-8f49-29c4fa560e17.png">

* Accuracy level is .648 which is not the best of all the models.
* The precision for high risk is minimum and for low risk is 1.
* Sensitivity here performs well but not perfect in both scenarios.
* The f1 score for low risk is .72 which means it could be a good model for this kind of loans.

### Balanced Random Forest Classifier

<img width="500" alt="Screen Shot 2022-10-26 at 16 36 20" src="https://user-images.githubusercontent.com/104656920/198143186-1c79d51a-1fda-4c17-8d69-351d89735455.png">

* Accuracy level in this model is far better than the last ones getting a .788 which means is capable to get good predictions for true positives and 
* High risk precision is still low in this model, however, it performs better than the last ones also.
* The sensitivity in both scenarios is higher than in the other models getting a .70 nand . 87 for high and low risk loans respectively.
* The f1 score for low risk is .93 which means this model is the best yet to predict this type of loans.

### Ease Ensemble AdaBoost Classifier

<img width="724" alt="Screen Shot 2022-10-26 at 16 37 47" src="https://user-images.githubusercontent.com/104656920/198143390-f86d0ba1-4c9d-429f-bb2e-0631000bb0d5.png">

* Accuracy level in this model is .932, making this model the best to predict correctly.
* High risk precision is still low in this model, however, it performs better than the last ones also.
* The sensitivity in both scenarios is higher than in the other models getting a .94 nand . 92 for high and low risk loans respectively, making this model effective to detect each of the classes.
* The f1 score for low risk is .97 making this model the best of all tested model for low risk and also has the highest score for high risk with .16



## Summary

We can see that different approaches in machine learning will also give different results. It was tested the 6 different methods of machine learning and while a lot of them seem very similar in the results the slightest change could help us to decide between one or the other model.

If we focus our attention in the best and worst performing methods we can analyze better why it is important in looking for the best option.

In this array we had 17,104 low_risk loans and 101 high risk loans. 

Undersampling model had a correct prediction of 70 high risk correct but 31 were not labeled as high risk, meanwhile the Ease Ensemble gives us 93  correct prediction out of the 101 high risk loans. Because is a high risk obviously having even 1 is a lot of risk and might mean losses to the company but it is very important to look in the impact a bad model can affect directly to the economics of a company and decisions.

When looking into the lower risk loans the undersampling also performs badly because it is labeling 10,324 as high risk, from a total of 17,104.

In summary it is important to test different Machine Learning methods in order to find one that will help get predictions or sensitivity high depending on what are the needs of the model. For example here talking about credit risk it is very important to have a more effective precision than sensitivity, because the need of spotting bad deals that might mean loss of income.
