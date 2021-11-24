# DSND_CNN_Dog_Detector
For Udacity Data Science Nanodegree

[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"
[image2]: ./images/vgg16_model.png "VGG-16 Model Keras Layers"
[image3]: ./images/vgg16_model_draw.png "VGG16 Model Figure"


### Table of Contents
  1. [Project Overview](#1--project-overview)
  2. [Installation](#2--installation)
  3. [File Descriptions](#3--file-descriptions)
  4. [Results](#4--results)
  5. [Licensing, Authors, and Acknowledgments](#5--licensing-authors-and-acknowledgments)

## 1. Project Overview
The goal of this project was to build a dog breed classifier which takes a user-supplied image as input and detects whether the image contains a dog or a human. If a dog is detected, the classifier also returns the breed of dog; if a human is found, the classifier returns what dog breed the person most resembles.

![Sample Output][image1]

The classifier uses a Convolutional Neural Network (CNN) and transfer learning to identify dog breeds for the predictions. 

## 2. Installation
This was a guided project; the data and some of the base code were provided by Udacity. Due to the size of the files the download locations are linked below rather than included in this repository. 

1. Clone the repository and navigate to the downloaded folder.
```	
git clone https://github.com/khiara/DSND_CNN_Dog_Detector.git
cd dog-project
```

2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 

3. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 

4. Download the bottleneck features for the dog dataset transfer learning, and place it in the repo, at location `path/to/dog-project/bottleneck_features`.
* [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz)  
* [ResNet-50 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogResnet50Data.npz)
* [Inception bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz)
* [Xception bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogXceptionData.npz)

Dependencies
* Python v3.*
* sklearn
* numpy
* matplotlib
* pandas
* keras
* glob
* cv2
* tqdm
* PIL


## 3. File Description

* [haarcascades](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/haarcascades) -- Folder containing OpenCV's Haar features based Cascading Classifier for human face detection
* [images](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/images) -- Folder containing sample images for notebook instructions
* [extract_bottleneck_features.py](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/extract_bottleneck_features.py) -- Functions to extract bottleneck features (code provided by Udacity)
* [dog_app.ipynb](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/dog_app.ipynb) -- The dog breed classifier notebook


## 4. Results
A full write up of the findings and my analysis can be found in a Medium post [here](https://medium.com/@k.chinn/             ).

## 5. Licensing, Authors, and Acknowledgments
Thanks go to [Udacity's](https://Udacity.com) Data Science Nanodegree Program for the project idea, datasets, and code framework, and to their mentors and community for guidance, tips, and encouragement. 
