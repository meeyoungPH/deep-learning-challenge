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
- After selecting the features, the data were transformed using the StandardScaler function.

## Compiling Training, and Evaluating the Model
- Initial neural network model
![one_node](output/one_layer.png)
   - The first model consisted of one input layer with one node and 43 features, one hidden layer with 22 nodes and ReLu activation, and an output layer with 1 node with sigmoid acivation. 
   - Relu was chosen for the hidden layer due to its constant gradient which contributes to faster learning. For the output layer, sigmoid functions are best to use for binary classification.
- Target model performance for the initial model was not achieved, with accuracy only reaching 0.7282.
- Optimized neural network model
   - The following manual steps were taken to optimize the neural network model in multiple iterations, none reaching an accuracy over 75%: changed the number of nodes in the first hidden layer, added second hidden layer, changed activation type of hidden layers, and applied weighted clustering with varying numbers of clusters.
![two_nodes](output/two_layers.png)
   - Next, kerastuner was applied to find the hyperparameters which would output the best model.
![kt](output/kt.png)

## Summary
The first model, with just one hidden relu layer and 22 nodes, resulted in an output just shy of the 75% target.
![first_model](output/first_model.png)

The second model, with an attempt to optimize by manually including an additional layer and other parameters, did not increase accuracy.
![second_model](output/second_model.png)

Finally, the last model was optimzed using kerastuner to identify the best hyperparameters for the optimal model. This resulted in the best model, which unfortunately was still shy of the 75% target.
![hp_model](output/hp_model.png)

## Discussion
Because this model is for binary classifcation of ventures as either successful or not based on various features, it lends itself well to a random forest classifier model. This model creates decision trees to generate class predictions based on samples of the dataset. The ensemble result of the decision trees then provide a prediction that is more accurate than the sum of its parts.

