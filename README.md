# Dog_Breed_Classifier
Udacity (Project 2) Dog Breed Classifier with PyTorch.

This is a repo for the Dog Breed Classifier Project in Udacity Nanodegree.
It is implemented by using PyTorch library.
Udacity's original repo is : [Repository](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-dog-classification)

## Project Overview
In this project,a pipeline is built that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, the algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

![alt text](https://github.com/udacity/deep-learning-v2-pytorch/raw/master/project-dog-classification/images/sample_dog_output.png)

Along with exploring state-of-the-art CNN models for classification and localization, important design decisions about the user experience is made for the app. The goal by completing this lab is to understand the challenges involved in piecing together a series of models designed to perform various tasks in a data processing pipeline. Each model has its strengths and weaknesses, and engineering a real-world application often involves solving many problems without a perfect answer. Your imperfect solution will nonetheless create a fun user experience!

## Datasets
1. To Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and the dogImages/folder should contain 133 folders, each corresponding to a different dog breed.
2. To Download the [human dataset](http://vis-www.cs.umass.edu/lfw/lfw.tgz).Unzip the folder.

## Creating a CNN to Classify Dog Breeds (From Scratch)
(conv1):Conv2d(3,32,3,stride=2,padding=1)<br />
activation: relu<br />
(pool): MaxPool2d(2)<br />
(conv2):Conv2d(32,64, 3,stride=2,padding=1)<br />
activation: relu<br />
(pool): MaxPool2d(2)<br />
(conv3):Conv2d(64,128, 3, padding=1)<br />
activation: relu<br />
(pool): MaxPool2d(2)<br />
(conv4):Conv2d(128,256, 3, stride=2, padding=1)<br />
activation: relu<br />
(fc1):Linear(4*4*256,1024)<br />
activation: relu<br />
(dropout):Dropout(0.25)<br />
(fc2):Linear(1024,512)<br />
activation: relu<br />
(dropout):Dropout(0.25)<br />
(fc3):Linear(512,133)<br />
(dropout):Dropout(0.25)<br /><br /> 
After training this model for 50 epochs :  Test Loss: 3.767316  Test Accuracy: 14% (122/836)  

## Creating a CNN to Classify Dog Breeds (using Transfer Learning)
Used ResNet152 for transfer Learning.\
After training the model for 25 epochs:  Test Loss: 0.944494  Test Accuracy: 75% (627/836)
