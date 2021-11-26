# DSND_CNN_Dog_Detector
For Udacity Data Science Nanodegree

[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"
[image2]: ./images/success_dog.PNG "Correct id"
[image3]: ./images/fail_dog.PNG "Incorrect id"
[image4]: ./images/success_dog2.PNG "Correct id"
[image5]: ./images/Afghan_Faye.PNG "Human"


### Table of Contents
  1. [Project Overview](#1--project-overview)
  2. [Installation](#2--installation)
  3. [File Descriptions](#3--file-descriptions)
  4. [Results](#4--results)
  5. [Licensing, Authors, and Acknowledgments](#5--licensing-authors-and-acknowledgments)

## 1. Project Overview
The goal of this project was to build a dog breed classifier which takes a user-supplied image as input and detects whether the image contains a dog or a human. If a dog is detected, the classifier also returns the breed of dog; if a human is found, the classifier returns what dog breed the person most resembles. If no dog or human is detected, the classifier returns an error.

![Sample Output][image1]

The classifier uses a Convolutional Neural Network (CNN) and transfer learning to identify dog breeds for the predictions. 

## 2. Installation
This was a guided project; the data, notebook, and base code were provided by Udacity. Building, training, and testing the models was done in a Udacity GPU-enabled classroom workspace. Due to the size of the files the download locations are linked below rather than included in this repository.  

Full instructions on how to install the project are [here](https://github.com/udacity/dog-project/blob/master/README.md).

1. Clone the repository and navigate to the downloaded folder. Rename as desired ('dog-project' used here as a standin).
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

5. Code to use on a local machine is located in the [requirements folder](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/requirements). List of dependencies is in [requirements.txt](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/requirements/requirements.txt) or [requirements-gpu.txt](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/requirements/requirements-gpu.txt).

6. Navigate to the main dog-project directory, open dog_app.ipynb and follow the instructions to run the cells.


## 3. File Description

* [haarcascades](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/haarcascades) -- Folder containing OpenCV's Haar features based Cascading Classifier for human face detection
* [images](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/images) -- Folder containing sample images for notebook instructions
* [requirements](https://github.com/khiara/DSND_CNN_Dog_Detector/tree/main/requirements) -- Folder containing code for running locally on different systems.
* [extract_bottleneck_features.py](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/extract_bottleneck_features.py) -- Functions to extract bottleneck features (code provided by Udacity)
* [dog_app.ipynb](https://github.com/khiara/DSND_CNN_Dog_Detector/blob/main/dog_app.ipynb) -- The dog breed classifier notebook


## 4. Results
The initial CNN created from scratch did not perform very well, with test accuracy of 10.2871%. A model using Xception bottleneck features for transfer learning improved performance significantly, with test accuracy of 82.8947%, but was much better identifying images from the provided files than unseen, user-provided images.

A full write up of the findings and my analysis can be found in a Medium post [here](https://medium.com/@k.chinn/identifying-dog-breeds-from-photos-using-cnns-and-transfer-learning-beee3ec065d8).           ).

### Sample images

![Correct id][image2]     A correctly identified dog from the training set  

![Incorrect id][image3]    An incorrectly classified user image

![Correct id][image4]     A correctly identified user image (same dog as in the previous image)

![Human][image5]    A human image from the provided dataset



## 5. Licensing, Authors, and Acknowledgments
Thanks go to [Udacity's](https://Udacity.com) Data Science Nanodegree Program for the project idea, datasets, and code framework, and to their mentors and community for guidance, tips, and encouragement. 
