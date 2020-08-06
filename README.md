# Snapchat_filter_using_facial_key_points

## Dataset 
The dataset is in the form of csv file and is available on kaggle(https://www.kaggle.com/c/facial-keypoints-detection/data).
The data contains of a csv file cosisting of pixel values of images as string and coordinates of key_points corresponding to images.

## Methodolgy for creating model
The Dataset is augmented by flipping the images and changing the contrast of the image.I then used an RNN trained on the subset of the augmented dataset with Adam optimizer and loss as categorical cross entropy using evaluation metrics as accuracy metrics.I saved the weights in .hdf5 file and the architecture of the RNN model in 
KeyPointDetector.json file.

Here is a blog post for how Adam optimizer works(https://medium.com/@h2knitt/momentum-rmsprop-and-adam-optimizer-5769721b4b19)
## Detecting the faces
I have used haarcascade frontal face classifier to detect multiple faces in the open cv video frames

## facial key points detection 
The images of the faces captured by haarcascade clssifier is resized and converted into dezired format and feed into RNN model to predict facial Key points

## Applying filters
These facial key points are used for applying the filters 
