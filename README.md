# **SDC-FindingLaneLines**

# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

## Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

To complete the project, two files will be submitted: a file containing project code and a file containing a brief write up explaining your solution. We have included template files to be used both for the [code](https://github.com/udacity/CarND-LaneLines-P1/blob/master/P1.ipynb) and the [writeup](https://github.com/udacity/CarND-LaneLines-P1/blob/master/writeup_template.md).The code file is called P1.ipynb and the writeup template is writeup_template.md 

To meet specifications in the project, take a look at the requirements in the [project rubric](https://review.udacity.com/#!/rubrics/322/view)

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

![image1](/images_for_writeup/1_originalImage.jpg)

---

## Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

This project is divided into 4 categories. First, color selection, second, canny edge detection, third, determining region of interest, and forth, hough transform for detecting lines.

My pipeline consisted of 10 steps. 

1. Convert RGB image to HLS color space
\
![image1](/images_for_writeup/2_hlsImage.jpg)

2. Create white and yellow color masking of the original RGB image
\
![image1](/images_for_writeup/3_maskedImage.jpg)

3. Convert white and yellow masking image to Grayscale color
\
![image1](/images_for_writeup/4_grayImage.jpg)

4. Smooth out the Grayscale image using Gaussian
\
![image1](/images_for_writeup/5_blurImage.jpg)

5. Use Canny edge detection function to detect edges of the image
\
![image1](/images_for_writeup/6_edgeImage.jpg)

6. Create region of interest
\
![image1](/images_for_writeup/7_maskedEdgeImage.jpg)

7. Use Hough tranform function to locate lines
\
![image1](/images_for_writeup/8_lineImage.jpg)

8. Use average function to calculate averaged slope and intercept of each lines and classify lanes as left or right

9. Draw new averaged lines on the image
\
![image1](/images_for_writeup/9_improvedLineImage.jpg)

10. Combined line image with original RGB image
\
![image1](/images_for_writeup/10_combinedImage.jpg)

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...