# Stereo-Disparity
Computer Vision Stereo Disparity

## Introduction
Stereo matching is the problem of finding correspondences between two images that are taken simultaneously from two cameras that are mounted so that they are parallel and separated along their x-axis. The output of stereo matching is a disparity image that, for every pixel in the left image (x), indicates how many pixels to the left its correspondence (x’) is in the right image, giving the disparity (x-x’).

<img width="379" alt="image" src="https://user-images.githubusercontent.com/88305416/208822436-0ff9fd46-ade1-4512-92f6-ad4f4fc3d529.png">

<img width="763" alt="image" src="https://user-images.githubusercontent.com/88305416/208822475-67d0750c-6454-422c-89c1-f9f5b08438b3.png">

## Dataset
The dataset is curated from https://drivingstereo-dataset.github.io

The images have been renamed so that they have the form:
* <something>-left.jpg 
* <something>-right.jpg 
* <something>-disparity.png
The left and right images are 8 bit rgb images. The disparity images are 16 bit monochrome images.

## Tasks
1. Calculate a disparity map for the left image using classical (non deep learning) methods
2. Calculate some statistics using supplied ground truth depth images
<img width="415" alt="image" src="https://user-images.githubusercontent.com/88305416/208823995-89f6a8a2-d61e-490b-8ef1-9ac60338f137.png">

## Approach
### Scan line
<img width="401" alt="Scan line" src="https://user-images.githubusercontent.com/88305416/208824095-bf8c8ea3-83a6-42e0-9ca3-ad01b37f1e88.png">

### Search box
![Search box](https://user-images.githubusercontent.com/88305416/208824113-fd84275a-06ac-4aa7-9c78-7dd083b55052.jpg)

### Acceleration
![cv_report](https://user-images.githubusercontent.com/88305416/208824240-181632bf-f34b-44ef-9be9-1e407ecb4634.jpg)

## Result
Score 20/25
