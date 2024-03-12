# Module 21 - Neural Networks and Deep Learning

## Neural Network Model Report

### Overview:

The purpose of this analysis is to create a binary classifier that can predict whether applicants will be successful if funded by the nonprofit foudnation, Alphabet Soup. I obtained the "charity_data.csv" dataset from the Alphabet Soup business team. 

The dataset included the following columns:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

Initially (Step 1: Preprocess the Data and Step 2: Compile, Train, and Evaluate the Model), I created a script (["Step_1_and 2.ipynb"](https://github.com/rperez025/deep-learning-challenge/blob/main/Deep%20Learning%20Challenge/Step_1_and_2.ipynb)) to preprocess the data, and then compilied, train, and evaluated the data for use with TensorFlow model. 

Additionally (Step 3: Optimized the Model), I created a second script (["Step_3.ipynb"](https://github.com/rperez025/deep-learning-challenge/blob/main/Deep%20Learning%20Challenge/Step_3.ipynb)) to optimize the Model by adjusting the input features to ensure that no variables or outliers are causing confusion in the model, for example: 
* Dropping more or fewer columns.
* Creating more bins for rare occurrences in columns.
* Increasing or decreasing the number of values for each bin.
* Add more neurons to a hidden layer.
* Add more hidden layers.
* Use different activation functions for the hidden layers.
* Add or reduce the number of epochs to the training regimen.

### Results: 
Using bulleted lists and images to support your answers, address the following questions:

* **Data Preprocessing**
  
  - What variable(s) are the target(s) for your model?
    * The target variable for the model is the IS_SUCCESSFUL column.
    
  - What variable(s) are the features for your model?
    * The features variables for the model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
    
  - What variable(s) should be removed from the input data because they are neither targets nor features?
    * I removed the EIN and NAME features since they do not have a meaningful relationship with the outcome/analysis.

* **Compiling, Training, and Evaluating the Model**
  
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * Initiall
  
  - Were you able to achieve the target model performance?
  
  - What steps did you take in your attempts to increase model performance?

### Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
