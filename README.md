# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.
The purpose of this project is to use the dataset to assist the foundation in predicticting where to make investments. Using the featires in the data set a binary classifiier was created that is capabel of predicting a succesful candidate for funding from Alphabet Soup. The data set consistis of more than 34,000 organizations that have recieved funds from Alphabet Soup. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME**_AMT—Income classification
* **SPECIAL**_CONSIDERATIONS—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
#### What variable(s) are considered the target(s) for your model?
 IS_SUCCESSFUL 
#### What variable(s) are considered to be the features for your model?
APPLICATION_TYPE AFFILIATION CLASSIFICATION USE_CASE ORGANIZATION STATUS INCOME_AMT ASK_AMT
#### What variable(s) are neither targets nor features, and should be removed from the input data?
EIN NAME SPECIAL_CONSIDERATIONS
### Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
This deep-learning neural network model is made of 5 hidden layers with 80, 40, 20, 10, and 5 neurons.
The input data has 43 features and 25,724 samples.
The output layer is made of a unique neuron as it is a binary classification.
The activation function ReLU was used for the hidden layers. THe output is a binary classifier, so the Sigmoid activation is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
#### Were you able to achieve the target model performance?
The model was unable to acheinve the specified 75% accuracy. Regardless of the model used the accuracy remained at .728 (+/- .03).
#### What steps did you take to try and increase model performance?
The first step was to eliminate features that were not contributing to the model- EIN NAME SPECIAL_CONSIDERATIONS
Then 3 vairables were bucketized- APPLICATION_TYPE CLASSIFICATION INCOME_AMT
A variety of nodes adn hidden layers were added to the model in an effort to increase accuracy. 
2 layers with 80 and 40 nodes- .723
4 layers with 20, 10, 5, 2 nodes- .726
5 layers with 100, 50, 20, 10, 10 nodes- .727
5 layers with 80, 40, 20, 10, 5 nodes- .728
Differnt activation functions were also tried including Sigmoid, Relu, and tahn. 
Regardelss of the specified model accuracy remined low. 
## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
The deep learning nueral network model did not reach the 75% accuracy target for identifying charity investments. Future modeling should include other binary classifiers such as logistic regression or Support Vector Machines to start with a more simplistic or straight forward model.

## Resources
https://www.tensorflow.org/api_docs/python/tf/keras/optimizers

https://github.com/borkard/Neural_Network_Charity_Analysis

https://www.tensorflow.org/api_docs/python/tf/keras/losses

https://github.com/emmanuelmartinezs/Neural_Network_Charity_Analysis

https://www.tensorflow.org/guide/keras

https://www.analyticsvidhya.com/blog/2021/08/a-beginners-guide-to-machine-learning-binary-classification-of-legendary-pokemon-using-multiple-ml-algorithms/

