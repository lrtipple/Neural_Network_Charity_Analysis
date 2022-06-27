# Neural_Network_Charity_Analysis

### Resources
jupyter, SciKit-Learn, charity_data.csv, Pandas, Tensorflow

## Overview
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

This new assignment consists of three technical analysis deliverables and a written report. You will submit the following:

- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: A Written Report on the Neural Network Model (README.md)

### Results

####  Data Preprocessing
- What variable(s) are considered the target(s) for your model?
  - Predictions are based on the "IS_SUCCESSFUL' column   
- What variable(s) are considered to be the features for your model?
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT  
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - EIN and NAME   

#### Compiling, Training, Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - This neural network model uded binary data and the first attempt I used 2 re hidden layers with 80 and 30 neurons and relu activation functions, and an output         layer with a sigmoid activation function. The neural network model was used due to the size of the data. 
  
 ![model1](https://user-images.githubusercontent.com/99093289/175844573-8d0d9d88-5853-465e-90de-62ee123b0653.PNG)

- Were you able to achieve the target model performance?
  - This model achieved 72.5% accuracy and 56.4% loss
  
 ![model1_acc](https://user-images.githubusercontent.com/99093289/175844593-fe9d6a27-7098-4469-a865-1ba5a0700b9b.PNG)

- What steps did you take to try and increase model performance?
  - I attempted three times to optimize the model's accuracy and lessen the loss, however I was unsuccessful. 
    - First Optimization - I added a third hidden layer with 10 additional neurons 
    
    ![modelOpt1](https://user-images.githubusercontent.com/99093289/175844957-f924b51a-a742-4a36-834a-df79020ddf0b.PNG)

    - Second Optimization - I increased the neurons in the first layer to 90, and 40 in the second layer
    
    ![modelOpt2](https://user-images.githubusercontent.com/99093289/175845001-d01e704e-c93a-466f-b3ad-db28bf229ed4.PNG)

    - Third Optimization - I decreased the epochs to 75 and the first hidden layer's neuron's to 50, and second layer to 25
    
    ![modelOpt3](https://user-images.githubusercontent.com/99093289/175845016-db71c7e3-73c8-4848-8ed5-7e06291aa86f.PNG)
    ![model3Opt_eph](https://user-images.githubusercontent.com/99093289/175845027-4202dbe9-5ddb-47b7-b220-081705e0bad1.PNG)

 ####  Summary
Overall, I was not successful in creating a good model using relu activation with this data. Each optimization change still resulted in 56% loss and only 72% accuracy. This means that over 50% of the time the model was not predicting accurately. 

### Recommendation  
I think we should try to use a different type of machine learning, like Random Forest, to increase the accuracy of the model for this data. I think there is too much categorical data considerations for this model to be successful using a binary only network.

