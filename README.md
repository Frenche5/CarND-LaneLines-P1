# **Finding Lane Lines on the Road** 


**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[pipeline](.\writeup images\process_image.jpg)
[result](.\writeup images\challenge_result.jpg)

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 8 steps. 
First of all I transform the image to grayscale, that way it is easier and more efficient to work with it.

Second, I make a Gaussiablur filter. This filter avoid the noise in the image, and make it smoother. This step avoid error in the next steps.

Third. In this step I apply the cany filter, which is basicaly an gradient edge detector which helps us to identify the basic shapes in the image.

Fourth. Mask image. In order to avoid unnecessary information, a mask is made to the image, focusing on the areas of importance, and where the information of the lines is most likely to be.

Five. In this step i apply the HoughLinesP function which detect lines in the image.

Six. In this step i made a algorithm where i calculated two average lines. I also made a filter with the slope to avoid lines close to horizontality.

Seven. With the lines calculated in the previous step i display the lines in a image.

Eight. In this step i mix both images, the original and the lines image.

![pipeline](.\writeup images\process_image.jpg)

![result](.\writeup images\challenge_result.jpg)



### 2. Identify potential shortcomings with your current pipeline


First shortcoming, is unsolved, and sometimes the video process give a error and only process a part of it.

Secodn issue, is that in the challenge video, the lines it is not so stable as i wanted.


### 3. Suggest possible improvements to your pipeline

A posible improvement to the pipeline, could be improve the slope filter and the HoughLinesP function, because this low stability in the lines may be because we are detecting incorrect lines that deviate when making the mean.
"# CarND-LaneLines-P1" 
