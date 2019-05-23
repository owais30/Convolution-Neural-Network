# Convolution-Neural-Network

In this repo, we will understand convolution neural network by looking at its architecture and algorithms....

# Understanding convolution neural network.....

# Lets look at the problem space..
  Given an input image, our developed algorithm must be able to identify the objects in it.   Image classification is the task of taking an input image and outputting a class (a cat, dog, etc) or a probability of classes that best describes the image.

# Input and Output
 When a computer sees an image (takes an image as input), it will see an array of pixel values. Depending on the resolution and size of
the image, it will see numbers like X * Y * Z, where Z = 1 if the image is gray scaled(Black_and_white) or Z = 3 if image is
colored(RGB).
Every pixel in the image is value ranging from 0 - 255.
The idea is that you give the computer this array of numbers and it will output numbers that describe the probability of the image being
a certain class (.80 for cat, .15 for dog, .05 for bird, etc).

# How to do this...
### We have solution for this task. We can use non deep learning model of deep learning models.
### These non deep learning models are outdated and perform less accurate than deep learning models.
###  Lets look at deep learning models..

# CNN
In neural networks, Convolutional neural network (ConvNets or CNNs) is one of the main categories to do images recognition, images
classifications. Objects detections, recognition faces etc., are some of the areas where CNNs are widely used.
CNN image classifications takes an input image, process it and classify it under certain categories (Eg., Dog, Cat, Tiger, Lion). 
Technically, deep learning CNN models to train and test, each input image will pass it through a series of convolution layers with filters
(Kernals), Pooling, fully connected layers (FC) and apply Softmax function to classify an object with probabilistic values between 0 and
1. The below figure is a complete flow of CNN to process an input image and classifies the objects based on values.

![Image](/Image/LeNet.png)

## Convolution Layer
Convolution is the first layer to extract features from an input image. Convolution preserves the relationship between pixels by learning
image features using small squares of input data. It is a mathematical operation that takes two inputs such as image matrix and a filter
or kernal
Consider a 5 x 5 whose image pixel values are 0, 1 and filter matrix 3 x 3 as shown in below

![Conv](/Images/1_MrGSULUtkXc0Ou07QouV8A.gif)

 After sliding the filter over all the locations, you will find out that what you’re left with an array of numbers, which
 we call an activation map or feature map.
 
 ### Stride
 Stride is the number of pixels shifts over the input matrix. When the stride is 1 then we move the filters to 1 pixel at a time. When
 the stride is 2 then we move the filters to 2 pixels at a time and so on.
 
 ### Padding
 Sometimes our filter doesn't fit exactly to the input image. So we add an extra column or row of zeros. This process is called as
 padding.
 
 ### Non Linearity..
 ReLU is a function used to remove non positive values from output array(output from the convolution layer.)
 
 ## Pooling layer
 This is the next layer in cnn process. Pooling layer has a window like 3 x 3 and operation like averaging. This window slides over the 
 output array(output from convolution layer) and perform operation on every step.
 Operations : Max, Average, Sum
 Example of max pooling..
 
 ![Pooling](/Images/1_SmiydxM5lbTjoKWYPiuzWQ.png)
 
 ## Fully connected layer
 
 ![Fully](/Images/1_Mw6LKUG8AWQhG73H1caT8w.png)
 
 Fully connected layer is final layer of CNN. 
 Output from the pooling layer is 2d array but fully connected layer expects input in the form of 1d array.
 So, first 2d array must be converted to 1d array by flattening it.
 Now, 1d array is passed to fully connected layer and this layer will output array of probability for every class.
 We select the class with highest probability.
 
 # CNN 
 
 ![Final](/Images/1_4GLv7_4BbKXnpc6BRb0Aew.png)
 
