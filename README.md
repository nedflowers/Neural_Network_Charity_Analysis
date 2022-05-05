# Neural Network Charity Analysis

## Overview

With neural networks and machine learning, use the features in the provided dataset to create a binary classifier that can accurately and efficiently predict whether applicants will be successful if funded.
Begin by preprocessing the data to use in a Neural Network Model. Next, compile, train, and evaluate the model. Then, restructure the model in three different ways to ensure optimization. Finally, provide a written analysis of the findings. 

## Results

### Data Preprocessing
-	What variable(s) are considered the target(s) for your model?
    - The target for the model is the ‘IS_SUCCESSFUL’ column

-	What variable(s) are to be the features for your model?
    - 'APPLICATION_TYPE',
    - 'AFFILIATION',
    - 'CLASSIFICATION',
    - 'USE_CASE',
    - 'ORGANIZATION',
    - 'INCOME_AMT',
    - 'SPECIAL_CONSIDERATIONS',
    - 'ASK_AMT'

-	What variable(s) are neither targets nor features, and should be removed from the input data?
    - The EIN and NAME columns were removed, as they are unnecessary for the model’s purpose.

### Compiling, Training, and Evaluating the Model

-	How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - My first model had 2 layers. One with 80 neurons and the second with 30. This resulted in 5,981 parameters. 
    - I thought 2 layers was a good starting point as I could see the model’s weak points at a base level.

-	Were you able to achieve the target model performance?
    - Though, I attempted to optimize my model, I was unable to reach accuracy over 73%, during 100 epochs. 

-	What steps did you take to try and increase model performance?
    - For my first optimization attempt, I binned the “ASK_AMT” column, to reduce noise after encoding, and I added an extra layer to my model.
    - The second optimization used tanh instead of relu activation.
    - My final optimization added 20 neurons to each layer, using relu activation.

## Summary

Overall, the model failed to reach over 73% accuracy in any of my attempts at optimization. I thought binning the 'ASK_AMT' column would be helpful in reducing noisy variables. Though binning helped, it did not significantly affect the outcome of the model. If we were to run the model for more epochs, we may reach a number closer to 75%, but that will take time, create further training loss, and take up more memory. 
Since the model’s purpose is to predict and categorize if a charity organization’s funding request is approved or not, we are looking at a binary solution. This means we can use a supervised machine learning model like Random Forest Classifier to generate decision trees and compare the performance to our Neural Network model. 
