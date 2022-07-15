# Neural_Network_Charity_Analysis

## Overview of Analysis:
Client requested a machine learning model that predicts how successful an applicatn will be if functed by their charity based of the provided data. The main focus is to use a Neural Network, however, other models are explored. 

## Resources
- Source Data: charity_data.csv
- Software: Python 3.10 (64-bit), Jupyter Notebook 6.4.8

## Results

### Data Preprocessing
What variable(s) are considered the target(s) for your model?

- The IS_SUCCESSFUL column was the target for this model.

What variable(s) are considered to be the features for your model?

- The following columns were consider to be features in the model:
  - AFFILIATION—Affiliated sector of industry
  - CLASSIFICATION—Government organization classification
  - USE_CASE—Use case for funding
  - ORGANIZATION—Organization type
  - STATUS—Active status
  - INCOME_AMT—Income classification
  - SPECIAL_CONSIDERATIONS—Special consideration for application
  - ASK_AMT—Funding amount requested

What variable(s) are neither targets nor features, and should be removed from the input data?

- The EIN and NAME columns were columns used for identification and were not included as a feature or a target.


### Compiling, Traning, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

- I used the kerastuner package to optimize the number of layers and nodes. The results can be seen below.

<p align="center">
  <img src="https://github.com/justinkirk8/Neural_Network_Charity_Analysis/blob/main/images/optimization.png" width="700" />
</p>

Were you able to achieve the target model performance?

- No, none of the adjustments I attempted increased the accuracy above 0.73 to the target of 0.75. I was able to get some models to 0.74 during training, however, they still did not increase above 0.73 when using test sets.

What steps did you take to try and increase model performance?

- I used kerastuner to optimize the number of layers and nodes
- I binned the ask ammount column in order to reduce noise
- I attempted to increase and decrease the number of epochs
- I attempted to drop various columns to see if they were confusing the model
- I also tried using the following seperate models:
  - Logistical Regression - best accuracy observed: 0.720
  - Random Forest -         best accuracy observed: 0.725
  - SVM -                   best accuracy observed: 0.718



## Summary


