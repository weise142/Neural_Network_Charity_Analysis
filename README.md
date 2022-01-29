# Neural_Network_Charity_Analysis
## Overview
The objective of this project was to analyse a dataset of over 34,000 organizations that have been funded by Alphabet Soup and then use machine learning and neural networks to try and predict if the applicants that will be funded by Alphabet Soup will be successful. The project comprised of 3 steps:
- Preprocessing the data for the neural network
- Compile, train, and evalute the model
- Optimize the prediction model
## Results
### Data Preprocessing
Based on the project goals and the dataset we determine the target for our model is the Is_Successful column. We then need to determine if we will be dropping any of the columns in the dataset, which we determine that the EIN and Name columns are not needed for our prediction model. The rest of the data is potentially useful so we leave the remaining data to be used in our model. 
### Compiling, Training, and Evaluating the Model
For the neural network model, I had 2 hidden layers. My first layer had 80 neurons, the second layer had 30 neurons and there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid". We can see that the accuracy of this model was about 71%
![This is an image](https://github.com/weise142/Neural_Network_Charity_Analysis/blob/main/accuracy%20module%202.PNG)
Next will be our attempts to increase the accuracy of the neural network to meet our goal of 75% accuracy. My first attempt I removed additional features, which was the Use_Case column, while keeping the rest of the information the same. This reduced the accuracy slightly to about 70%
![This is an image](https://github.com/weise142/Neural_Network_Charity_Analysis/blob/main/accuracy%20attempt%201.PNG)
For the second attempt I added additional neurons to the hidden layers and aditional hidden layers are added. Despite adding additional neurons, the accuracy of the model went down to about 48%
![This is an image](https://github.com/weise142/Neural_Network_Charity_Analysis/blob/main/accuracy%20attempt%202.PNG)
For the third attempt, I changed the activation function of the output layer from "sigmoid" to "tanh". Again the accuracy of the model went down, this time to about 45% the lowest of the attempts.
![This is an image](https://github.com/weise142/Neural_Network_Charity_Analysis/blob/main/accuracy%20attempt%203.PNG)
## Summary
After making tweaks to the neural network the model accuracy was below 50% while the initial neural network we setup had an accuracy of about 71% allmost meeting our 75% goal. The loss in accuracy can be explained because we overfit the model to try and increase the accuracy of our target column Is_Successful. By overfitting our model and either removing data or adding additional neurons we reduced the accuracy. If we contrinue to use neural networks we should revert back to our initial model since it had the highest accuracy score or we could make some changes such as increasing the amount of data we feed into our network. Another option would be to use the Random Forest Classifier as this is another accurate model that can take into account the large dataset and produce accurate results due to its sufficient number of estimatorsand tree depth. The random forest classisfers are generally faster than neural networks because we dont have to train them so we could use that speed to potentially avoid overfitting the model.
