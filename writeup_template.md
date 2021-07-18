# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report
---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

MMy pipeline consisted of 5 steps. First, I converted the images to grayscale,
then I blurred the image a little bit using the gaussian_blur function. Then, 
I applied the canny edge detection function on my image. 
Then I extracted the region of interest from the image based on the vertices that I draw. 
After that, I applied Hough transformation on that image. 
Finally, I added both photo the original one with the one resulted from Hough transform.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by
calculating the gradient and the intercept. 
Then created two list for positives and negative gradients and for the left and right intercepts. 
then calculated the mean of each list. Then calculated x1, y1, x2,y2

If you'd like to include images to show how the pipeline works, here is how to include an image: 



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the lane lines are curved not straight


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to develope the pipeline to detect curved lane lines.