# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidYellowCurve2.jpg "solidYellowCurve2.jpg"
[image2]: ./test_images_output/whiteCarLaneSwitch.jpg "whiteCarLaneSwitch.jpg"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied Gaussion smoothing before
using Canny edge detection, which is useful to get an image of edges. I continued to define a region of interest in the
edges-image from the Canny edge detection because the lane lines should be in the bottom of the picture. After that
I applied Hough detection to find the relevant lines in the region of interest.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by extrapolating the
lines from the Hough detection. I separated these line dependent from their slope to the left or the right lane. After that the
x and y coordinates for the lines are calculated and the whole line is plotted.

Here are 2 images after the addition of the red lane lines:

![image1]: [image1]
![image2]: [image2]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
