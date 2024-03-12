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

* Dropping more or fer columns.
* Creating more bins for rare occurrences in columns.
* Increasing or decreasing the number of values for each bin.
* Add more neurons to a hidden layer.
* Add more hidden layers.
* Use different activation functions for the hidden layers.
* Add or reduce the number of epochs to the training regimen.

### Results: 

* **Data Preprocessing**
  
  - What variable(s) are the target(s) for your model?
    
    * For Step 1, 2, and 3, the target variable for the model is the IS_SUCCESSFUL column.
    
  - What variable(s) are the features for your model?
    
    * For Step 1 and 2, the features variables for the model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
    
    * For Step 3, the features variables for the model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT.
    
  - What variable(s) should be removed from the input data because they are neither targets nor features?
    
    * For Step 1 and 2, removed the EIN and NAME features since they do not have a meaningful relationship with the outcome/analysis.
    
    * For Step 3, removed EIN again, hover, decided to remove STATUS, and SPECIAL_CONSIDERATIONS features since there are small percentages of projects that are in the minority categories.
      
* **Compiling, Training, and Evaluating the Model**
  
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    
    * For Step 1 and 2, the sequential model included:
      - Nuerons:
        * 1st layer = 80
        * 2nd layer = 30
        * 3rd layer = 1
      - Layers = 3
      - Activation functions:
        * 1st and 2nd layers = Rectified Linear Unit ('ReLU')
        * 3rd layer = Sigmoid
      - Epochs = 100

    * For Step 3, the sequential model included:
      - Nuerons:
        * 1st layer = 100
        * 2nd layer = 30
        * 3rd layer = 10
        * 4th layer = 1
      - Layers = 4
      - Activation functions:
        * 1st layer = ReLU
        * 2nd, 3rd, and 4th layers = Sigmoid
      - Epochs = 100

    Initially (Step 1 and 2), I selected the neurons, layers, activation functions, and epochs based on best practices to determine initial evaluation of the model. Upon determining that the model's performance did not exceed the target accuracy of 75%, I modified the neurons, layers, and activation functions to improve the model's performance in achieving a target accuracy exceeding 75%.
  
  - Were you able to achieve the target model performance?
    
    * For Step 1 and 2, the model resulted in 72.83% accuracy, which did not meet the target model performance for higher than 75%. Therefore, performed optimization on the model (Step 3) and achieved 79.17% accuracy, which exceeded the 75% target model performance.
  
  - What steps did you take in your attempts to increase model performance?
    * For Step 3: Optimization, I performed the following to increase model performance:
      - Maintained the NAME column and continued to drop the EIN column, as well as the STATUS and SPECIAL_CONSIDERATIONS columns.
      - Performed binning procedures over the NAME column.
      - Modified the number of layers, nodes per layer, and activation functions. Please refer to "Compiling, Training, and Evaluating the Model" section above for details.

### Summary: 

Overall, the results of the TensorFlow deep learning model indicate that it did increase performance from 72.83% to 79.17% accuracy based on adjusting/increasing the number of neurons and layers, as well as applying different activation functions. I would recommend to use a Random Forest Classifier model as an alternative to the TensorFlow model on the dataset. This is based on fitting and evaluating the Random Forest Classifier (See last section in  ["Step_3.ipynb"](https://github.com/rperez025/deep-learning-challenge/blob/main/Deep%20Learning%20Challenge/Step_3.ipynb)) resulting in 77.76% accuracy. Although it did not exceed the accuracy of the optimized TensorFlow model (79.17%), it still exceeded the target accuracy score of 75%.
