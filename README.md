# Plagiarism detector model deployment using SageMaker

## Introduction

This is a project from Udacity's Machine Learning Engineer Nanodegree. The data was provided by Udacity. The data consists of 100 students' short answers to 4 types of questions and their corresponding wikipedia answers. These wikipedia answers serve as the source texts to compare against the students' answer texts. The plagiarism detector model will classify a student's answer text as either somewhat plagiarised from the wikipedia source or not plagiarised. In the original dataset, the answer texts are being classified into 4 different types of plagiarism based on its severity of the plagiarism. For classification purpose, the dataset only uses 0 -- original answer and 1 -- plagiarised answer -- as labels.

## Model

* Logistic Regression and XGBoost are used
* train.py contains sklearn logistic regression model
* In the notebook XGBoost section, I employed SageMaker built-in XGBoost model

## Result

* Both algorithm gives 100% test accuracy.
* This is reasonable because the test size is rather small -- 25 answer texts.
* SageMaker built-in XGBoost algorithm takes much longer time to train the model in comparison to the sklearn logistic regression.
* See details on hyperparameters used in the notebook.
* Possible improvement points
   1. Fine tune hyperparameters
   2. Shuffle training data
   3. Improve feature engineering
   4. feature selection step can be guided by statistical tests
   
 ## Source
 __Udacity Machine Learning Nanodegree__
 [dataset corpus source](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html)

