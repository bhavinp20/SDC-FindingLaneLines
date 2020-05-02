# SDC-FindingLaneLines

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

![image1](/images/1_originalImage.jpg)

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

This project is divided into 4 categories. First, color selection, second, canny edge detection, third, determining region of interest, and forth, hough transform for detecting lines.

My pipeline consisted of 10 steps. 

1. Convert RGB image to HLS color space
\
![image1](/images/2_hlsImage.jpg)

2. Create white and yellow color masking of the original RGB image
\
![image1](/images/3_maskedImage.jpg)

3. Convert white and yellow masking image to Grayscale color
\
![image1](/images/4_grayImage.jpg)

4. Smooth out the Grayscale image using Gaussian
\
![image1](/images/5_blurImage.jpg)

5. Use Canny edge detection function to detect edges of the image
\
![image1](/images/6_edgeImage.jpg)

6. Create region of interest
\
![image1](/images/7_maskedEdgeImage.jpg)

7. Use Hough tranform function to locate lines
\
![image1](/images/8_lineImage.jpg)

8. Use average function to calculate averaged slope and intercept of each lines and classify lanes as left or right

9. Draw new averaged lines on the image
\
![image1](/images/9_improvedLineImage.jpg)

10. Combined line image with original RGB image
\
![image1](/images/10_combinedImage.jpg)

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
