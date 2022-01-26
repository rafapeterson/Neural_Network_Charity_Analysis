# Neural_Network_Charity_Analysis
## Overview
The purpose of this analysis was to run predictive models to determine the most successful funded organizations by Alphabet Soup Charity. 

## Results
### Data Preprocessing
<li> The variable considered a target for the model was "IS_SUCCESSFUL." Using this target, we were able to analyze and predict future success based on the features of the model</li>
<li> The variables considered to be features were as follows: Application Type, Affiliation, Classification, Use Case, Organization type, Status, Income Amount, Special considerations, and Ask amount.</li>
<li> The other variables, EIN & Name, were not important to this research, so they were removed. 
</li>
List of variables used: <br> <img src="https://user-images.githubusercontent.com/13009587/151244190-7c395a45-38fc-4f91-8986-3d73ce0e3868.png">
<br><br>
### Compiling, Training, and Evaluating the Model
<li> For this project, the following specifications were used: 2 layers, one with 80 neurons & the other with 30. Both used the Relu activation function, plus the output layer used the Sigmoid function. 2 layers were used because the data was not linear: there were many factors impacting whether the candidate was successful or not. Upon researching an adequate number of layers to use, through <a href="https://machinelearningmastery.com/how-to-configure-the-number-of-layers-and-nodes-in-a-neural-network/">"How to configure the number of layers and nodes in a neural network"</a> I decided to try two layers, as "...there is a theoretical finding by Lippman in the 1987 paper 'An introduction to computing with neural nets' that shows an MLP with two hidden layers is sufficient for creating classification regions of any desired shape." The number of nodes was decided upon initially based on the starter code, but was later altered to add more neurons in order to perform a more in depth analysis. The configurations were chosen at random.</li>
<br>
<li> I was <u>not</u> able to achieve the target model performance. The first attempt resulted in an accuracy score of ~54%. <img src="https://user-images.githubusercontent.com/13009587/151245951-5d58db66-d4c7-4064-9ef1-d6c0b8d0c358.png"></li>
<li> Three attempts were made to improve the accuracy:
  <ol> <li>In the first, USE_CASE was also removed as a beneficial column. <img src="https://user-images.githubusercontent.com/13009587/151246675-8e46704c-458a-403a-9357-d2d853679221.png">. Also, the criteria for application type being labeled as "other" was increased to 500, in an attempt to optimize the data further. With these changes, the accuracy score increased to ~64%. <img src="https://user-images.githubusercontent.com/13009587/151247384-207dba1a-3497-4f16-9bcd-6dc337ebbe9c.png">
    </li> 
  <li> In the second attempt, the same changes made in attempt one were used, along with increasing the threshold for a Classification to be considered "Other" from 500 to 1000 entries within each category. Again, this was implemented to further widdle down the data. <img src="https://user-images.githubusercontent.com/13009587/151247906-6d176063-8f4a-447c-9c02-ef8ac2a97347.png"> The results from this test increased slightly, with an accuracy score of ~65%. <img src="https://user-images.githubusercontent.com/13009587/151248052-234ae334-4ae1-4e21-84ec-d46ba864defe.png">
</li>
<li> For the third, and final attempt, the variables adjusted in the first 2 were first reverted back to the original test. Then, one of the changes made in this attempt was to increase the criteria for application type being labeled as "other" up to a minimum of 1000 entries. Similarly, the criteria for Classification to be labeled "other" was increased to 1500. <img src="https://user-images.githubusercontent.com/13009587/151249823-1a932f4f-fc31-4a07-aa50-b2d96f8ad088.png">. Also, the hidden nodes in both layers were doubled in this test, to see if a more thorough review of data would impact accuracy. <img src="https://user-images.githubusercontent.com/13009587/151250122-f523a230-0153-44d2-ba0f-c48b82615e92.png"> With this test, the results were an accuracy score of ~64%. <img src="https://user-images.githubusercontent.com/13009587/151250558-55f4e8eb-8e1b-4039-90fc-e9971d0e3eeb.png">. </li></ol>
  
  ## Summary
  Overall, this deep learning model was not successful at achieving an accuracy score of 75% or better. To increase the result, trying a RandomForest model may be a better option, as the Random Forest utilizes many models to come to a conclusion, which may mirror the various tests completed with the neural network, while being less prone to overfitting. 
  




