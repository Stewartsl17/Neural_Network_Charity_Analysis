# Neural_Network_Charity_Analysis

## Objective 

Based on our previous work with machine learning models that utilized neural networks, we were asked to develop another machine learning model to predict whether or not applicants will be successful if funded by Alphabet Soup. We were given a CSV containing over 30,000 organizations that have received funding over the years from Alphabet Soup. 

In order to develop the machine learning model using neural networks, we did the following: 

* Preprocess the Data
* Compile, Train, and Evaluate the Model
* Optimize the Model

## Results 

### Preprocessing the Data 

In order to correctly create the model, we had to remove the EIN and NAME, as well as, the ASK_AMT variable. We deleted the first two variables because they don't add value to the accuracy of the model. We removed the last variable because the variable counts were too varied in comparison to the rest of the data. The final list of feature variables is: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, STATUS. The target variable for our model is IS_SUCCESSFUL.

### Compiling, Training, and Evaluating the Model

In our original model, we were able to achieve a performance level of 72.55%, which was a good first trial of the model. However, we were then asked to reach a model performance level of 75%. In order to do so, we tested several different shifts in various features of the model, including: 

* Dropping a Column <br>
![](https://github.com/Stewartsl17/Neural_Network_Charity_Analysis/blob/main/Images/Option%201%20-%20Remove%20a%20Column.png)

* Increasing Neurons <br>
![](https://github.com/Stewartsl17/Neural_Network_Charity_Analysis/blob/main/Images/Option%202%20-%20Increase%20Neurons.png)

* Adding a Hidden Layer <br>
![](https://github.com/Stewartsl17/Neural_Network_Charity_Analysis/blob/main/Images/Option%203%20-%20Add%20Hidden%20Layers.png)

* Changing the Activation Types <br>
![](https://github.com/Stewartsl17/Neural_Network_Charity_Analysis/blob/main/Images/Option%204%20-%20Use%20Different%20Activation%20Functions%20.png)

The best shift of the features tested was the third option, which was the addition of another layer. The number of hidden layers was 3 and the number of neurons per layer was 80/30/5. Based on modeling practices and other testing, we found that 2 times the number of outputs was best for our top layer and then to follow the other best performing sizes from past tests for the other layers. This model also continued to utilize the relu activation for the hidden layers and the sigmoid for the output layer because these were best performing during testing. <br>
![](https://github.com/Stewartsl17/Neural_Network_Charity_Analysis/blob/main/Images/Option%203%20Layers.png)

However, despite this being our best model, we did not achieve the asked performance level of 75%. 

## Summary 

We were asked to create a machine learning model that utilized neural networks that could be used to predict if applicants will be successful if they are funded by Alphabet Soup. Based on the CSV datafile that we were given, we created a machine learning model that produced a 72.55% accuracy. After being asked to optimize the model to have a 75% level of accuracy, we tried 4 shifts to the features in order to achieve this: Dropping a Column, Increasing Neurons, Adding Hidden Layers, and Changing the Activation Types. Based on those tests, our highest model output produced was 72.92%. This does not pass the asked performance level. To further improve this model and its performance, we could utilize more basic supervised machine learning models such as Random Forest. This would best handle the type of data that this CSV file is, as well as, the type of model that Alphabet Soup needs for their ask.
