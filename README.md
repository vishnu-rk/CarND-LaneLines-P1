# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

# *Reflection*

*A simple 7 step pipeline for finding road lanes is described below.*

1. Grayscale the given image using
2. Blur it using gaussian kernal for smoothening the image
3. Use Canny edge detection to find edges all over the image.
4. Filter the edges using prior knowledge of approximate lane location. This area is the region of interest.
5. Use Hough Transform to find lines from edges in the region of interest.
6. Filter out outliers within output of lines from above step based on a slop filter
7. Calculating average slope of both lines and extrapolate lines to the correct coordinates based on initial assumption for region of interest.


*Possible shortcomings*
1. Pipeline might fail during low/no light conditions.
2. Pipeline might fail if lane markings donot stand out visually.

*Possible improvements*
1. We could use GPS information to predict lane markings along with visual information. Not sure how to combine the two data properly though.
2. Use lidar data of vehicles moving in the vicinity to create a pattern and assist lane prediction.


