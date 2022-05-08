# Neural_Network_Charity_Analysis

## Overview of Project
In this project I use machine learning models to abnalyze applcations for donation fundings to see which applicants will be able to use it effectively.

### Purpose

**Analytical:** I deploy neural network models to determine whether or not the applicant will be successful in utilizing the funding as intended.

**Technical:** TensorFlow, Scikit-learn and Pandas libraries were employed


## Results

#### Data Preprocessing
1. The variable "IS_SUCCESFUL" was used as the target for the model, as it conatained the results of funding being used effectively. This column became the most important, because if the applicants would not be succefful, then Alphabet Soup's funding would simply go tot waste.

2. Features used for the machine learning model - Application Type, Affiliation, Classification, Use case, Organization, Income Ammount, Special Considerations and Ask Amount

3. The columns EIN and NAME were dropped from the get go as those do not influence the outcome

#### Compiling, Training, and Evaluating the Model
1. 
| **Attribute** | **Selection** | **Reason** |
| --- | --- | --- |
| Neurons | first layer: 80<br>second layer: 30 | More number of neurons give a higher accuracy. *Therefore the neurons were increased in later attemps to achieve that* |
| Layers | 2 (and an output layer)| More number of layers improves performance, but a lower number runs the analysis faster [^1]<br>2 layers can represent accuracy with rational activation functions [^2] |
| Activation Functions | Rectified Linear Unit (relu) | "relu" function is the most advanced function [^3] |

[^1]: `https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw`
[^2]: `https://medium.com/geekculture/introduction-to-neural-network-2f8b8221fbd3`
[^3]: `https://www.aitude.com/comparison-of-sigmoid-tanh-and-relu-activation-functions/#:~:text=ReLu%20is%20the%20best%20and,compare%20to%20other%20activation%20function.`
2. The target accuracy was 75%, however 53.38% was achieved in the first attempt. Certain modifications were made to improve the accuracy and the highest value achieved was **60.75%**

3. The following 3 attemps were made at improving the accuracy: 

| **Attempt** | **Change** | **Resulting Accuracy** |
| --- | --- | --- |
| 1 | Removing redundant features | ![ 1 ](/Resources/accuracy_1.png) | 
| 2 | Adding additional neurons and layers | ![ 2 ](/Resources/accuracy_2.png) | 
| 3 | Changing activation function | ![ 3 ](/Resources/accuracy_3.png) |

As can be seen in the table above, the first two attempts resulted in improving the accuracy achieved in the original attempt (53.38%)

Unfortunaetly, changing the activation function from "sigmoid" to "relu" in the output layer reduced the accuracy.

## Summary

The model achieved an accuracy of 60.75% after optimization. 

Unfortunately, the consistent low accuracy of the models implies the data is being **overfitted**, suggesting that the dataset is missing some key features that would truly determine the success/failure of the applicant.

Because this is a binary classification problem, a supervised machine learning model can be used:

1. **Random Forest Classifiers** can be used instead of Neural Networks, as the former is more robust due to the number of estimators and tree depth. 
2. **SVM** can be used as they aren't prone to overfitting and do not converge on a local minima, unlike Neural Networks.

