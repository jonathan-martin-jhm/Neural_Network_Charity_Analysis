# Neural_Network_Charity_Analysis

## Overview of The Analysis

Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME — Identification columns
* APPLICATION_TYPE — Alphabet Soup application type
* AFFILIATION — Affiliated sector of industry
* CLASSIFICATION — Government organization classification
* USE_CASE — Use case for funding
* ORGANIZATION — Organization type
* STATUS — Active status
* INCOME_AMT — Income classification
* SPECIAL_CONSIDERATIONS — Special consideration for application
* ASK_AMT — Funding amount requested
* IS_SUCCESSFUL — Was the money used effectively

### Goals of The Project
* Deliverable 1: Preprocessing Data for a Neural Network Model
* Deliverable 2: Compile, Train, and Evaluate the Model
* Deliverable 3: Optimize the Model
* Deliverable 4: A Written Report on the Neural Network Model (README.md)


## Results

### Data Preprocessing

#### What variable(s) are considered the target(s) for your model?

* APPLICATION_TYPE — Alphabet Soup application type
* AFFILIATION — Affiliated sector of industry
* CLASSIFICATION — Government organization classification
* USE_CASE — Use case for funding
* ORGANIZATION — Organization type
* STATUS — Active status
* INCOME_AMT — Income classification
* SPECIAL_CONSIDERATIONS — Special consideration for application
* ASK_AMT — Funding amount requested
   
    
#### What variable(s) are considered to be the features for your model?

* IS_SUCCESSFUL — Was the money used effectively 

#### What variable(s) are neither targets nor features, and should be removed from the input data?

* EIN and NAME — Identification columns


### Compling, Traning, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
* The intial model contained three hidden layers. Hidden layer one, two, and three had 80, 30, and 1 neuron(s), respectively. The number of neurons, were chosen to approximately double the input layers and minimize overfitting. The activation function of the first two were chosen to be "relu" to restrict the outcomes from 0 to infinity and the final output layer was "sigmoid" to produce a binary predictive outcome. 


#### Were you able to achieve the target model performance?
* No, the target model performance was to achieve a predictive accuracy >75%. The best model had a predictive accuracy of 72.6% and the initial model had a predictive accuracy of 72.5%. Minimal, if any, improvements were made to the model in the optimization attempts. 


#### What steps did you take to try and increase model performance?
* Initial Model

Loss: 0.5554019212722778, Accuracy: 0.7252478003501892


* Optimization Attempt 1: The USE_CASE column was removed because I deemed this to be a noisy column that would not influence the status of the loan approval process.

Loss: 0.5604059100151062, Accuracy: 0.7261807322502136


* Optimization Attempt 2: The neurons used in the hidden layers were doubled in an attempt to improve the predictive accuracy.

Loss: 0.5660737156867981, Accuracy: 0.726064145565033


* Optimization Attempt 3: An extra hidden layer with the "tanh" was added to expand the predicted outcomes to include negative values.

Loss: 0.5599883198738098, Accuracy: 0.7250145673751831



## Summary
In the project, achieving a predictive accuracy of >75% was not acheived using a neural network model with 3 attempts at optimization. The best attempt only achieved a predictive accuracy of 72.6%. Further attempts could be made with the neural network model to reduce loss and increase accuracy by removing more columns that are likely causing overfitting reduce the number of epochs, and more layers could be added to improve the accuracy. Alternatively, I would recommend trying other machine learning models to improve the predictive accuracy. Since neural networks are prone to overfitting and are more difficult to train, as such a logistic regression model could be generated in an attempt to minimize the amount of trouble shooting involved with neural networks.
