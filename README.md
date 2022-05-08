# Neural_Network_Charity_Analysis

## Overview of Project
In this project I let supervised machine learning analyze 6 different models for sampling data for credit card applications, to determine whether or not the applicants qualify.

### Purpose

**Analytical:** I deploy supervised machine learning models to determine the eligibility of applicants for credit card loans. I analyze the confusion matrix to determine false negatives/positives and true negatives/positives to understand the precision and accuracy of each model

**Technical:** *Packages* - numpy, numpy-base, numpydoc <br> *Libraries* - NumPy, SciPy, Scikit-learn, Pandas


## Results

#### Data Preprocessing
1. 
2. 
3. 

#### Compiling, Training, and Evaluating the Model
1. 
2. 
3. 

| Attempt | Change | Resulting Accuracy |
| --- | --- | --- |
| 1 | Removing redundant features | ![ 1 ](/Resources/accuracy_1.png) | 
| 2 | Adding additional neurons and layers | ![ 2 ](/Resources/accuracy_2.png) | 
| 3 | Changing activation function | ![ 3 ](/Resources/accuracy_3.png) |

<p align="left">
<img src="/Resources/eec.png" width="70%" height="35%">
</p>

|  | **Scores** |
| --- | --- |
| Balanced Accuracy | 93% [^2] |


[^2]: `https://github.com/RababHanda/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb`

## Summary

The scores for high risk loans will be used to compare the different models because that is the constraint that will majorly affect the company giving out loans. Cost of low risk applicants being wrongly determined eligible won't pose much of a risk to the company.
