# Neural_Network_Charity_Analysis

## Overview of Project
In this project I let supervised machine learning analyze 6 different models for sampling data for credit card applications, to determine whether or not the applicants qualify.

### Purpose

**Analytical:** I deploy supervised machine learning models to determine the eligibility of applicants for credit card loans. I analyze the confusion matrix to determine false negatives/positives and true negatives/positives to understand the precision and accuracy of each model

**Technical:** TensorFlow, Scikit-learn and Pandas libraries were employed


## Results

#### Data Preprocessing
1. The variable "IS_SUCCESFUL" was used as the target for the model, as it conatained the results of funding being used effectively. This column became the most important, because if the applicants would not be succefful, then Alphabet Soup's funding would simply go tot waste.

2. Features used for the machine learning model - Application Type, Affiliation, Classification, Use case, Organization, Income Ammount, Special Considerations and Ask Amount

3. The columns EIN and NAME were dropped from the get go as those do not influence the outcome

#### Compiling, Training, and Evaluating the Model
1. | **Attribute** | **Selection** | **Reason** |
| --- | --- | --- |
| Neurons | first layer: 80<br>second layer: 30 | More number of neurons give a higher accuracy. *Therefore the neurons were increased in later attemps to achieve that* |
| Layers | 2 (and an output layer)| More number of layers improves performance, but a lower number runs the analysis faster [^1]<br>2 layers can represent accuracy with rational activation functions [^2] |
| Activation Functions | Rectified Linear Unit (relu) | "relu" function  |

[^1]: `https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw`
[^2]: `https://medium.com/geekculture/introduction-to-neural-network-2f8b8221fbd3`

2. 
3. 

| **Attempt** | **Change** | **Resulting Accuracy** |
| --- | --- | --- |
| 1 | Removing redundant features | ![ 1 ](/Resources/accuracy_1.png) | 
| 2 | Adding additional neurons and layers | ![ 2 ](/Resources/accuracy_2.png) | 
| 3 | Changing activation function | ![ 3 ](/Resources/accuracy_3.png) |

<p align="left">
<img src="/Resources/eec.png" width="70%" height="35%">
</p>


## Summary

The scores for high risk loans will be used to compare the different models because that is the constraint that will majorly affect the company giving out loans. Cost of low risk applicants being wrongly determined eligible won't pose much of a risk to the company.
