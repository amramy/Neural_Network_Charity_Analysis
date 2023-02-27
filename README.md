# Neural Network Charity Analysis  

## Overview: 
Alphabet Soup has been contributing funds to 34,000 organizations over the years and has asked to create a neural network machine learning model to help predict if the money is helpful. Utilizing the features in the dataset provided to create a binary classifier that is capable of predicting weather applicants will be successful if funded by Alphabet Soup. 

## Results: 

**Data Preprocessing**  

* The target variable for this model is the "IS_SUCCESSFUL" column which consist of two values 0 representing not_successful and 1 representing True it is_successful.  

* The feature variables in this model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE,     ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.  

* As the Identification Number (EIN) and the Name were neither targets nor features these two columns were dropped from the input dataset. 

### Compiling, Training, and Evaluating the Model

* In the AlphabetSoupCharity Model a good place to start is with the Relu activation function accompanied with two layers the first having 80 nodes (neurons), the second layer with 30 nodes.   

* The target model performance of 75% was not achieved, the closest being 72%. 

* Different variations to the model including dropping another column, changing the test ratio, using different activation functions, adding hidden layers, changing the number of Epochs, and changing the amount of neurons. None of these variations were able to produce a model better than 72%.


### AlphabetSoupCharity Model Output:
Accuracy: 72.6%  Loss: 56%
* 100 Epochs
* Input Layer = Relu with 80 nodes
  * Second Layer = Relu with 30 nodes
<img width="398" alt="Initial Output" src="https://user-images.githubusercontent.com/111904266/221434686-cceb1976-0dcd-4586-81de-4c9ec6e64e30.png">



### Optimization_1: 
Accuracy: 63.2%  Loss: 63.3%  

**Modification**
* Dropped column "Affiliation"
* 50 Epochs
* Input Layer = Relu with 80 nodes
  * Second Layer = Relu with 30 nodes
  * Third Layer = Relu with 30 nodes
<img width="392" alt="Optimize-1" src="https://user-images.githubusercontent.com/111904266/221434690-2bde0418-5af0-4975-ade6-0774a709b42e.png">


### Optimization_2: 
Accuracy: 72.3%  Loss: 57.7%  

**Modification**
* Test_Size = 80% of data
* 100 Epochs
* Input Layer = Tanh with 80 nodes
  * Second Layer = Tanh with 30 nodes
<img width="392" alt="Optimize-2" src="https://user-images.githubusercontent.com/111904266/221434698-a5c79084-f205-4b86-9e03-815c0592dc4b.png">


### Optimization_3: 
Accuracy: 72.7%  Loss: 58.7%  

**Modifications**
* Test_Size = 70% of data
* 100 Epochs
* Input Layer = Tanh with 100 nodes
  * Second Layer = Tanh with 50 nodes
  * Third Layer = Relu with 30 nodes
<img width="407" alt="Optimize-3" src="https://user-images.githubusercontent.com/111904266/221434702-701791a6-a7a1-4a51-9d71-27a4f3066223.png">


### Optimization_4: 
Accuracy: 72.5%  Loss: 56%  

**Modifications**
* 50 Epochs
* Input Layer = Relu with 100 nodes
  * Second Layer = Relu with 50 nodes
  * Third Layer = Relu with 30 nodes
  * Forth Layer = Relu with 10 nodes
  <img width="395" alt="Optimize-4" src="https://user-images.githubusercontent.com/111904266/221434710-2f0ffad7-59cd-4867-b8fd-f2998f3874e7.png">


## Summary: 
After reviewing the results of the various models and not being able to achieve an accuracy with more than 72% accompanied with high loss percentage the next models to try would be SVM, as it is also a binary classifier, and RandomForrestClassifier.  

*****
### Resources: 
  
 **Data:**  
 * charity_data.csv
  
 **Tools/ Packages/ Libraries:**
 * Jupyter Notebooks
 * sklearn
   * train_test_split
   * StandardScaler
   * OneHotEncoder
 * Pandas
 * TensorFlow
   * ModelCheckpoint
  
  
  
