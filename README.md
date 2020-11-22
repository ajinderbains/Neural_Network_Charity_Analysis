# Neural Network Charity Analysis
## Overview
We will create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.[Charity Dataset](https://github.com/ajinderbains/Neural_Network_Charity_Analysis/blob/main/charity_data.csv) is provided and we will perform following operations to predict:
1. Dadat Manipulation/Processing

2. Create train and test dataset

3. Fit the model for train and test dataset

4. Train the dataset and find accuracy of train and test data to predict the accuracy of model

## Results
[AutoSoupCharity notebook](https://github.com/ajinderbains/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb) is used to process,train and fit the trained data in model.[AutoSoupCharity Optimization notebook](https://github.com/ajinderbains/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb) is used to optimize the model with different attempts by changing neurons,activation etc.
- Data Processing
  - Target is output value and we want to develop the model that predict if donation to campaign is successful so I have chosen "Is_Successful" column as target for model 
  -  Features are individual independent variables that act as the input in your system. Prediction models use features to make predictions. So in this data set I have taken features like "Application Type","Bins for donation amount".
  - "EIN" and "Name" neither are Targetnor features ,so we have dropped input dataset.

- Compiling,Training,Evaluating
  - In the first model  One input layer one hidden layer and output layer is used.
  - "Sigmoid" activation function is used for output layer and "Relu" activation code is uused for first/Input and second layer .
  - For input layer lenght of scaled trained is used and in next hidden layer 30 neurons are used .There will be les risk of overfitting if less neurons are used.
  - The Accuracy with this model is 0.7286 and round off value id 73%.
 
 - Optimization
    - Attempt-1
    
       Removed the 2 features 'SPECIAL_CONSIDERATIONS_N','SPECIAL_CONSIDERATIONS_Y' and trained,fit in model and accuracy for this model is 0.7307.
    
    - Attempt-2
   
        Removed the 2 features 'SPECIAL_CONSIDERATIONS_N','SPECIAL_CONSIDERATIONS_Y' ,added additional neuron from 30 to 80 and trained,fit in model and accuracy for this model          is 0.7262.
    
    - Attempt - 3
  
      Removed the 2 features 'SPECIAL_CONSIDERATIONS_N','SPECIAL_CONSIDERATIONS_Y'  added additional neuron from 30 to 80  in second layer ,added third layer with 20 neurons and       trained,fit in model and trained,fit in model and accuracy for this model is 0.7307.
    - Attempt - 4 
   
      Removed the 2 features 'SPECIAL_CONSIDERATIONS_N','SPECIAL_CONSIDERATIONS_Y'  added additional neuron from 30 to 80  in second layer ,added third layer with 20 neurons and       trained,fit in model,changed activation function from "Relu" to "tanh" and trained,fit in model and accuracy for this model is 0.7250.
      
 ## Summary
  So  after multiple optimation attempts the  best accuracy rate is 0.7307 when noisy features  'SPECIAL_CONSIDERATIONS_N','SPECIAL_CONSIDERATIONS_Y' are removed and added additional neuron from 30 to 80  in second layer and added third layer with 20 neurons.
  - Recommendation
  
  With current neural network,after splitting trained and test dataset and multiple optimization attempts the accuracy rate is around 72%.So we can conclude that accuracy rate is very consistent in neural data model and I will recommend same neural data model which is currently used for this analysis.
  
  
   
