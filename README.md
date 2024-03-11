# Deep-Learning

## Overview of the analysis: 

Alphabet Soup, a nonprofit foundation, is seeking a tool to assist in the targeted selection of funding applicants with the highest likelihood of success in their endeavors. Leveraging your expertise in machine learning and neural networks, your task is to utilize the features within the provided dataset to develop a binary classifier. This classifier will be designed to predict whether applicants stand a good chance of success when receiving funding from Alphabet Soup.

From Alphabet Soup's business team, you have been provided with a CSV file encompassing information on more than 34,000 organizations that have received funding from Alphabet Soup throughout the years. 

Results: Using bulleted lists and images to support your answers, address the following questions:

## Data Preprocessing

What variable(s) are the target(s) for your model?
'IS_SUCCESSFUL' is the target variable. This will allow to build a deep learning model to predict the successful campaigns.

What variable(s) are the features for your model?
This dataset includes various columns capturing metadata about each organization:
1. Identification columns like EIN and NAME, 
2. Alphabet Soup application type (APPLICATION_TYPE)
3. Affiliated sector of industry (AFFILIATION)
4. government organization classification (CLASSIFICATION)
5. use case for funding (USE_CASE)
6. organization type (ORGANIZATION)
7. active status (STATUS)
8. income classification (INCOME_AMT)
9. special considerations for application (SPECIAL_CONSIDERATIONS)
10. funding amount requested (ASK_AMT)
11. and the effectiveness of the funding usage (IS_SUCCESSFUL).

What variable(s) should be removed from the input data because they are neither targets nor features?
The 'EIN' and 'NAME' columns are removed because they are not necessary to train the model.


## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
![](images/model.png)

The initial neural network model, a two-layer architecture with specific parameters for the number of neurons, layers, and activation functions. The first hidden layer comprised 80 neurons (hidden_nodes_layer1 = 80), the second hidden layer had 30 neurons (hidden_nodes_layer2 = 30), and both hidden layers utilized the ReLU activation function (activation="relu"). This configuration of the neural network was selected to capture and comprehend meaningful patterns within the data. The ReLU activation function facilitated the introduction of non-linearity. A solitary neuron in the output layer (units=1) was employed, employing a sigmoid activation function (activation="sigmoid") to address the binary classification. The sigmoid activation function effectively maps a range between 0 and 1, which is useful in detecting probability.

![](images/model_accuracy.png)

Model Accuracy - 72.5%

Were you able to achieve the target model performance?

This model was not able to acheive the target of 75% accuracy.

## Attempts to increase model performance

### Optimization 1 - Adjust the number nodes per layer
![](images/Opt_1.png)

    i. Adjusting nodes from 80 to 50 in layer 1.
    ii. Adjusting nodes from 30 to 15 in layer 2.

![](images/Opt_1_accuracy.png)

##### Accuracy = 72.65% (almost no change)

### Optimization 2 - Adjust the number number of layers
![](images/Opt_2.png)

    i. Add third layer with same nodes as second layer in Optimization 1.

##### Accuracy = 72.44% (almost no change)

![](images/Opt_2_accuracy.png)

### Optimization 3 - Adjust the number drastically nodes per layers
![](images/Opt_3.png)

    i. Adjusting nodes from 80 to 7 in layer 1.
    ii. Adjusting nodes from 30 to 15 in layer 2.

![](images/Opt_3_accuracy.png)

##### Accuracy = 72.45% (almost no change)

## Summary 
The overall results show that the attempts to improve the model through optimization were minimal at best, and they did not reach the target of 75% accuracy. Although all the accuracy results were similar, the neural network that had the highest accuracy was Optimization 1 and this would be the recommended model to use with this dataset.

