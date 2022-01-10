# Challenge_wine_quality_deeplearning
First steps in deep learning and building neuronal network

## Mission objectives
Use a deep learning library
Prepare a data set for a machine learning model
Put together a simple neural network
Tune parameters of a neural network

## 4 steps to build a model in Keras

+ 1: Architecture = how many layers do you want? How many nodes in each layer? What activation function do you want to use in each layer?
+ 2: Compile the model = specify the loss function, details about “how optimisation works
+ 3: Fit the model = cycle of back-propagation and optimization of model weights with your data
+ 4: Use your model to make predictions

## steps

### 1: Sefine a treshold between what is a good wine and a bad wine 

good_wine = [7,8,9]
bad_wine = [3,4,5,6]

df.quality = df.quality.replace(to_replace=good_wine, value=1)
df.quality = df.quality.replace(to_replace= bad_wine, value=0)

On that way, the quality of the wines has been transformed to 0 or 1 in the same column.

### 2: Select the feature and the target

The features are the following: 

'fixed acidity', 'volatile acidity', 'citric acid',
'residual sugar', 'chlorides', 'free sulfur dioxide',
'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol'

The target is:

'quality'


### 3: Define the architecture of the model

Model:
The model that has been chosen is a regression. A Sequential algorithm has been selected as model constructor. Sequential models require that each layer has weights or connections only to the one layer coming directly after it in the network diagram.

Layers:
Some hidden layers have been added to the model with the add method. Dense layers have been selected. It is called Dense because all of the nodes in the previous layer connect to all of the nodes in the current layer. In each layer, we specify the number of nodes as the first positional argument, and the activation function we want to use in that layer (‘relu’) using the keyword argument activation. In the first layer, we need to specify input shapes that will have n_cols columns, and there is nothing after the comma, meaning it can have any number of rows, = any number of data points
The last layer has only one node. That is the output layer where we ended with a single node.

### 3:Compile the model
In this step, we add an optimizer 'adam' to control the learning rate, which means how quickly the model finds good weights.
We also add a loss function

### 4: Fit the model

When we train the model we have an accuracy of 76% 

### 5: Use your model to make predictions

The accuracy on the test_set is 81%

bGraphs to vizualize the training loss and the training accuracy 

![image](https://user-images.githubusercontent.com/84380205/132689245-bbbd28b7-4462-48c4-b2f2-3d864967c65a.png)

### 6: Confusion matrix

To compare our results with the predictions we use a confusion matrix

![image](https://user-images.githubusercontent.com/84380205/132694072-b80cf233-1644-438c-bedd-8d140244a7f3.png)


