# Challenge_wine_quality_deeplearning
First steps in deep learning and building neuronal network

## Mission objectives
Use a deep learning library
Prepare a data set for a machine learning model
Put together a simple neural network
Tune parameters of a neural network

## 4 steps to build a model in Keras

1: Architecture = how many layers do you want? How many nodes in each layer? What activation function do you want to use in each layer?
2: Compile the model = specify the loss function, details about “how optimisation works
3: Fit the model = cycle of back-propagation and optimization of model weights with your data
4: Use your model to make predictions

## steps

1: define a treshold between what is a good wine and a bad wine 
good_wine = [7,8,9]
bad_wine = [3,4,5,6]

df.quality = df.quality.replace(to_replace=good_wine, value=1)
df.quality = df.quality.replace(to_replace= bad_wine, value=0)

2: Define the architecture of the model


3:Compile the model

4: Fit the model

5: Use your model to make predictions

