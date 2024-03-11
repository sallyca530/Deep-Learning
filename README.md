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
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

