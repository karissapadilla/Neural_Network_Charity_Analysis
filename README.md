# Neural Network Charity Analysis

## Overview of the Analysis
The purpose of the analysis is to be able to predict whether applicants will be successful if funded by Alphabet Soup by using Machine Learning and Neural Networks.

## Results
### - Data Preprocessing</br>
#### ? What variable(s) are considered the target(s) for your model?
The target variable is “IS_SUCCESSFUL” column.
#### ? What variable(s) are considered to be the features for your model?
The following feature variables are the following: 
-	APPLICATION_TYPE
-	AFFILIATION
-	CLASSIFICATION
-	USE_CASE
-	ORGANIZATION
-	STATUS
-	INCOME_AMT
-	SPECIAL_CONSIDERATIOINS
-	ASK_AMT
#### ? What variable(s) are neither targets nor features, and should be removed from the input data? 
EIN and NAME variables were both removed from the analysis.

### - Compiling, Training, and Evaluating the Model
#### ? How many neurons, layers, and activation functions did you select for your neural network model, and why?
For the Base model, I used the following parameters:
-	2 hidden layers (80, 30 nodes respectively) using Relu activation to showcase classification
-	1 output layer using sigmoid to showcase binary classification
-	Epochs = 100
#### ? Were you able to achieve the target model performance?
Accuracy result was only 64% using the above parameters which was below the 75% desired result. 
![Base Model](./Images/Base%20Model%20Accuracy.png)
Image 1. Base Model Parameters

#### ? What steps did you take to try and increase model performance? 
Three optimization methods were tried:
Optimization #1 – Data binning/bucketing of the INCOME and AFFILIATION variables to reduce variation in the data.  
Optimization #2 – Using the original parameter of the Base model except for decreasing Epoch to 50 which resulted to a much lesser accuracy score of 48%.
![Epoch at 50](./Images/Epoch%20at%2050.png)
Image 2. Epoch at 50
Optimization #3 – Using the original parameter of the Base model except for changing activation to “tanh” to account for negative inputs; however, accuracy score was still at 48%.
![TANH Activation](./Images/TANH%20Activation.png)
Image 3. TANH Activation
Optimization #4 – For good measure, I added another optimization method which is to add another hidden layer to a total of three with 180, 100, and 50 nodes respectively.  Accuracy score was still at 48%.
![Additional Layer](./Images/Additional%20Layer.png)
Image 4. Additional Layer

## Summary
In summary, we were not successful in achieving an accuracy score of at least 75% using the current model and parameters as used in the analysis.  I would recommend the following:
-	Analysis of the data provided (we may need a lot more data to use in the model)
-	Using a custom activation model such as Leaky ReLU function for nonlinear input data with many negative inputs

