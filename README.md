# Alphabet Soupt Charity - Deep Learning Challenge
## Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Machine learning and neural networks are applied to the dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Data
From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

- EIN and NAME: Identification columns
- APPLICATION_TYPE: Alphabet Soup application type
- AFFILIATION: Affiliated sector of industry
- CLASSIFICATION: Government organization classification
- USE_CASE: Use case for funding
- ORGANIZATION: Organization type
- STATUS: Active status
- INCOME_AMT: Income classification
- SPECIAL_CONSIDERATIONS: Special considerations for application
- ASK_AMT: Funding amount requested
- IS_SUCCESSFUL: Was the money used effectively

## Data Preprocessing
- The target variable is 'IS_SUCCESSFUL', a flag to indicate whether past applicants were successful in their venture with funding from Alphabet Soup.
- The features for this model include: 
   - APPLICATION_TYPE
   - AFFILIATION
   - CLASSIFICATION
   - USE_CASE
   - ORGANIZATION
   - STATUS
   - INCOME
   - SPECIAL CONSIDERATIONS
   - ASK_AMT
- The EIN and NAME variables were removed since they were not features for the model

## Compiling Training, and Evaluating the Model
- Initial neural network model
   - The first model consisted of one input layer with one node and 43 features, one hidden layer with 22 nodes and ReLu activation, and an output layer with 1 node with sigmoid acivation. 
   - Relu was chosen for the hidden layer due to its constant gradient which contributes to faster learning. For the output layer, sigmoid functions are best to use for binary classification.
- 





### Overview

