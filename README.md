# Pneumonia Detection on Chest X-Ray images using Convolution Neural Networks

This Notebook shows how to perform pneumonia detection on Chest X-Ray images using data augmentation techniques and Convolution Neural Networks (CNNs). 
An analysis of the results including the confusion matrix and the ROC curve is given in the last part.

The dataset used can be found on kaggle at https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
This work is based on the paper "An Efficient Deep Learning Approach to Pneumonia Classification in Healthcare, Journal of Healthcare Engineering, 2019, Okeke Stephen et al".

## Random samples of the initial dataset:

![Alt text](images/INIT_DATA.png?raw=true "Random samples of the initial dataset")

It contains 3 sets (Training, Validation, Test) labeled in 2 classes (patient with or without pneumonia)  in the following proportions:

![Alt text](images/CHEST_X_RAY.png?raw=true "PIE")

As you see, our sets are not well balanced (we have more images of sick patient than healthy patient).

In order to balance our dataset, we will use Keras to generate new consistent images from our different sets with ImageDataGenerator.

The following settings will be used:
 
rescale = 1/255 (pixel normalization)
rotation_range = 40
width_shift_range = 0.2
height_shift_range = 0.2
shear_range = 0.2
zoom_range = 0.2
horizontal_flip = true

## Convolutional Neural Network

![Alt text](images/MODEL.png?raw=true "MODEL")

![Alt text](images/KERAS MODEL.png?raw=true "KERAS MODEL")

## Training
![Alt text](images/CNN_training_1.png?raw=true "CNN training")

## Results Analysis
### Confusion Matrix
![Alt text](images/CONFUSION_MATRIX.png?raw=true "CONFUSION MATRIX")

### ROC curve
![Alt text](images/ROC.png?raw=true "ROC")










