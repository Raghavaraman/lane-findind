# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

Pipeline
---

**The order of function calls and the expected outputs are as follows:**

1. Convert the input image into grayscale by calling fuction grayscale.
<img src="carnd outputs/grayscale.png" width="480"/>
2. Apply gaussian_blur on the grayscale image to reduce the noise.
3. Set low and high threshold and then call the canny function.
<img src="carnd outputs/canny_full.png" width="480"/>
4. Determine the vertices of the region of interest and apply the mask to get the road lines alone.
<img src="carnd outputs/canny_example.png" width="480"/>
5. Draw line on the identified lines using the hough transform.
<img src="carnd outputs/line.png" width="480"/>
6. Superimpose the drawn line on to the image.
<img src="carnd outputs/solidyellowleft.png" width="480"/>

Future Improvements
---

When applied on the video. The lines seem to shake a bit. Some sort of stablisation algorithm can be used to make sure the line are much more stable and less shaky.
