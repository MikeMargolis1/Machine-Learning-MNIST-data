# Machine-Learning-MNIST-data

In this project I will be creating a Conventional Neural Network and a machine learning algorithm in Python to identify hand-drawn images from the MNIST "train" dataset. In this project I will be only using Pandas and Numpy arrays to create the algorithm. 

The data in the MNIST dataset have 40,000 observations. For each observation the first column is an indicator value (0-9) that corresponds to the label of each hand drawn observation. Following the first column is 784 columns containing either a 1 or 2. These 784 columns correspond to a 28x28 matrix. A 1 indicates that a pixel in that matrix has information. When arranged in a 28x28 matrix, all the 1s or "lit up part of the image" form an image corresponding to a hand drawn image/value of 0-9. I randomly shuffle the data to allow for new observation to be added to the train and test sample each time the code is ran.

This Neural Net has one hidden layer and for activation I use a ReLu function. For the algorithms "guess" I will be using a SoftMax function.

I first created the forward propagation equations to allow for weights and biases to be added to each pixel as it is passed from layer to layer. The original weights and biases for each pixel are random and will be changed after back propagation and "learning".

For back propagation, I created equations to readjust the weights and biases after each guess. I had to use derivative to undo the forward propagation and adjustment for each term are based on. Multiplying the old parameter by the learning term and the variation of each guess. Next the parameters are updated based on a learning rate of 5%. 

For in and out of sample testing, the algorithm accurately predicted what to label the hand drawn images over 90% of the time beating the baseline of 10%.
