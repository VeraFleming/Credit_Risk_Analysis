# Credit_Risk_Analysis

## Overview of the analysis:

Using the imbalanced-learn and scikit-learn libraries, we will evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. 
First, we’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then we’ll use the undersampling ClusterCentroids algorithm.  Using these algorithms, we’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
 
 For Delivarable 2 we’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, we’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
 
 For Delivarable 3 we’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, using  imblearn.ensemble library to predict credit risk and evaluate each model. Using both algorithms, we’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Results:

First we have to do the essential steps to prepare data fo the Machine Learning:

1. Split the data into input and output.
2. Create an instance of the model.
3. Train the model with the dataset.
4. Validate the model.

- For Oversampling we used RandomOversampler to resample training data and Logistic Regression model to train resampled data. The balanced accuracy score for this model is 0,66 which is pretty low. The imbalanced classification report looks like folowing: 

<img src= "Pictures/imbalanced classification report.png" width = "500"> 

- Also, for Oversampling we used SMOTE Oversampling to resample training data and Logistic Regression model to train resampled data. The balanced accuracy score for this model is 0,64 which is pretty low. The imbalanced classification report looks like folowing: 

<img src= "Pictures/icr SMOTE.png" width = "500">

- For Undersampling we used ClusterCentroids to resample training data and Logistic Regression model to train resampled data. The balanced accuracy score for this model is 0,64 which is still pretty low. The imbalanced classification report looks like folowing: 

<img src= "Pictures/icr ClusterCentroids.png" width = "500">

And we used a combination of Over and Under Sampling which is called SMOTEENN. After we resampled data to train a logistic regression model the  balanced accuracy score calculated as 0,66 which is a little hihger then the previous models, but not much. The imbalanced classification report looks like folowing: 

<img src= "Pictures/icr SMOTEENN.png" width = "500">

For next we had to use ensemble classifiers. First we used BalancedRandomForestClassifier to resample the training data for same dataset. The calculated the balanced accuracy score for this model is 0,79 and imbalanced classification report looks like the following:

<img src= "Pictures/icr Forest Classifier.png" width = "500">

Then we used EasyEnsembleClassifier to resample the training data for same dataset. The calculated the balanced accuracy score for this model is 0,93 and imbalanced classification report looks like the following:

<img src= "Pictures/cri EasyEnsembleClassifier .png" width = "500">

## Summary: 

All models with resampling data showed pretty low accuracy score, but in the imbalanced classification report we can see that all models predicted low_risk better and a presision rate is 1 in all reports. The SMOTE model has better F1 score which is  0.81 and could be a possible choise for choosing a model for predictions in the certain circumstances.
The models with Ensemble Learners showed better results, especially EasyEnsembleClassifier showed accuracy score as 0,93 which is the highest from all the models, Also, its presision and F1 scores looks pretty high. So from all the presented models in this challenge the EasyEnsembleClassifier is recomendation to use.






