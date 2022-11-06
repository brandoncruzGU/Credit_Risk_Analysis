# Credit Risk Analysis

## Overview
This project uses supervised machine learning to compare different resampling models that assess credit card risk. Due to the unbalanced classification of credit risk, we will test several resampling models which include two machine learning models that are meant to reduce bias. This analysis provides an overview of the machine learning model results which include their balanced accuracy, precision, and recall scores. After presenting the results, we also provide a high-level summary and recommend which model best predicts credit risk.

## Results

###RandomOverSampler
![image](https://user-images.githubusercontent.com/107777321/200157564-506fe925-5b99-4a0b-9889-e686b0582448.png)
The first oversampling model that we will test is Naive Random Oversampling. The balanced accuracy score for the Naive Over Sampling model is 0.63. The precision score for high_risk  and low_risk predictions are 0.56 and 0.70 respectively. The recall scores for high_risk and low_risk predictions are 0.65 and 0.61.

###SMOTE OverSampling
![image](https://user-images.githubusercontent.com/107777321/200157597-4e126716-dbb4-4dbb-832d-fd9797f85800.png)
The second oversampling model that we used is the SMOTE Oversampling model. The balanced accuracy score for the SMOTE Over Sampling model is 0.64. The precision score for high_risk and low_risk predictions are 0.59 and 0.70 respectively. The recall scores for high_risk and low_risk predictions are 0.66 and 0.63.

###ClusterCentroid UnderSampling
![image](https://user-images.githubusercontent.com/107777321/200157631-a7ff2473-c4d9-4a3b-a26b-2cf5012ce536.png)
We then use an undersampling model, the Cluster Centroids model, to determine if undersampling algorithms perform better than oversampling. The balanced accuracy score for this model is 0.67. The precision scores for the high_risk and low_risk predictions are 0.64 and 0.70 respectively. The recall scores for the high_risk and low_risk predictions are 0.68 and 0.66.

###CombinatorialApproach using SMOTEENN
![image](https://user-images.githubusercontent.com/107777321/200157673-cc55df09-0ea9-4b4e-8e09-652398169dae.png)
We then test a model that combines over and under sampling using the SMOTEENN algorithms. The balanced accuracy score for this model is 0.63. The precision scores for the high_risk and low_risk predictions are 0.64 and 0.61. The recall scores for the high_risk and low_risk predictions are 0.65 and 0.61. 

###BalancedRandomForestClassifier
![image](https://user-images.githubusercontent.com/107777321/200157711-bcf96469-2d32-4862-96c1-c0d0dc730e73.png)
Lastly, we test two ensemble algorithms to determine if their results perform the best. The first ensemble algorithm we used is the Balanced Random Forest Classifier. The balanced accuracy score for this model is 0.94. The precision scores for the high_risk and low_risk predictions are 0.04 and 1.00. The recall scores for the high_risk and low_risk predictions are 1.00 and 0.88.

###EasyEnsembleClassifier
![image](https://user-images.githubusercontent.com/107777321/200157744-32c80257-7f2f-4506-a65c-00b46f1640e7.png)
The second and final ensemble model we test is the Easy Ensemble Ada Boost Classifier. The accuracy score of this model is 0.97. The precision scores for the high_risk and low_risk predictions are 0.08 and 1.00 respectively. The recall scores for the high_risk and low_risk predictions are 0.99 and 0.94.

##Summary and Recommendations
The oversampling, undersampling, and combined sampling algorithms have fairly similar accuracy, precision, and recall scores. They do not yield scores that are high enough for us to confidently predict the actual credit risk. 

The ensemble algorithms yield the highest balanced accuracy scores. These are significantly higher than the other sampling models, however, the precision scores for the high_risk predictions are extremely low and would not show many instances of actual clients with high credit risk. 

With all this in mind, it might be worthwhile to explore other machine learning models that would yield greater results. However, if the client were to choose from the tested models, then I would recommend to use the Easy Ensemble Classifier. The accuracy score and recall scores are higher than the other models which is more beneficial in this case scenario. Although there are a few clients who will inaccurately be marked as high risk, everyone who is actually high risk will be marked as well.

